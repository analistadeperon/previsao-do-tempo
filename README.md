# previsao-do-tempo
<script
  src="https://code.jquery.com/jquery-3.3.1.min.js"
  integrity="sha256-FgpCb/KJQlLNfOu91ta32o/NMZxltwRo8QtmkMRdAu8="
  crossorigin="anonymous"></script>

<img src='' id="icone Tempo" width="60px">
<br/>
<strong>Paraguaçu Paulista/SP</strong><br/>
<span id="temperatura"></span><br/>
<span id="clima"></span>
<span id="diario"></span><br>

<strong>Assis/SP</strong><br/>
<span id="temperatura"></span><br/>
<span id="clima"></span>
<span id="diario"></span><br>

<strong>Marilia/SP</strong><br/>
<span id="temperatura"></span><br/>
<span id="clima"></span>
<span id="diario"></span><br>

<button>aperte o botao + e saiba a temperatura da sua cidade</button>

<script>
$(document).ready(function(){
	$.get( "http://apidev.accuweather.com/currentconditions/v1/36728.json?language=pt&apikey=hoArfRosT1215", function(data) {
	$('#temperatura').html(data[0].Temperature.Metric.Value);
	$('#clima').html(data[0].WeatherText);
  $('#localização').html(local)[0].(WeatherText);
	$('#icone tempo').attr('src','https://vortex.accuweather.com/adc2010/images/slate/icons/' + data[0].WeatherIcon + '.svg');
	});
});
</script>
