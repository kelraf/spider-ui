<template>
  <div>
    <Breadcrumbs main="Dashboard" title="University"/>
    <!-- Container-fluid starts-->
    <div class="container-fluid">
      <div class="row">

        <div class="col-xl-6 xl-100">
          <div class="card" data-intro="This is University Earning Chart">
            <div class="card-header university-header">
              <div class="row">
                <div class="col-sm-6">
                  <h5>University Earning</h5>
                </div>
                <div class="col-sm-6">
                  <div class="pull-right d-flex buttons-right">
                    <div class="right-header">
                      <div class="onhover-dropdown">
                        <button class="btn btn-primary" type="button">Monthly <span class="pr-0"><i class="fa fa-angle-down"></i></span></button>
                        <div class="onhover-show-div right-header-dropdown"><a class="d-block" href="#">Average</a><a class="d-block" href="#">Maximum</a><a class="d-block" href="#">Minimum</a></div>
                      </div>
                    </div>
                    <div class="right-header">
                      <div class="onhover-dropdown">
                        <button class="btn btn-light" type="button">yearly <span class="pr-0"><i class="fa fa-angle-down"></i></span></button>
                        <div class="onhover-show-div right-header-dropdown"><a class="d-block" href="#">Average</a><a class="d-block" href="#">Maximum</a><a class="d-block" href="#">Minimum</a></div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <div class="card-body height-curves">
              <div class="curves-2">

                <chartist
                ratio="animate-curve ct-golden-section"
                type="Line"
                :data="animate_curve_chart.chartData"
                :options="animate_curve_chart.chartOptions" />

              </div>
            </div>
          </div>
        </div>

        <div class="col-xl-6 xl-100">
          <div class="row">
            <div class="col-md-6">
              <div class="card">
                <div class="card-body">
                  <div class="media feather-main">
                    <div class="feather-icon-block"><feather type="command"></feather></div>
                    <div class="media-body align-self-center">
                      <h6>Total Admission</h6>
                      <p>5678</p>
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <div class="col-md-6">
              <div class="card">
                <div class="card-body">
                  <div class="media feather-main">
                    <div class="feather-icon-block"><feather type="navigation"></feather></div>
                    <div class="media-body align-self-center">
                      <h6>Total University Visit</h6>
                      <p>8569</p>
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <div class="col-sm-6">
              <div class="card">
                <div class="card-body">
                  <div class="media chart-university">
                    <div class="media-body">
                      <h3 class="mb-0"><feather type="dollar-sign"></feather><span class="counter">5683</span></h3>
                      <p>Html Course</p>
                    </div>
                    <div class="small-bar">
                        <chartist
                        ratio="ct-small-left flot-chart-container"
                        type="Bar"
                        :data="widgetBar.data"
                        :options="widgetBar.options"
                        :event-handlers="widgetBar.eventHandlers" />
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <div class="col-sm-6">
              <div class="card">
                <div class="card-body">
                  <div class="media chart-university">
                    <div class="media-body">
                      <h3 class="mb-0"><feather type="dollar-sign"></feather><span class="counter">7243</span></h3>
                      <p>PHP Course</p>
                    </div>
                    <div class="small-bar">
                      <chartist
                        ratio="ct-small-right flot-chart-container"
                        type="Bar"
                        :data="widgetBar.data"
                        :options="widgetBar.options"
                        :event-handlers="widgetBar.eventHandlers" />
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <div class="col-md-6">
              <div class="card">
                <div class="card-header">
                  <h5>Math Professors</h5>
                </div>
                <div class="card-body">
                  <div class="table-responsive professor-table mb-0">
                    <table class="table table-bordernone">
                      <tbody>
                        <tr>
                          <td><img class="img-radius img-35 align-top m-r-15 rounded-circle" src="../../assets/images/university/math-1.jpg" alt="">
                            <div class="professor-block d-inline-block">luson keter
                              <p>Math Professors</p>
                            </div>
                          </td>
                          <td>
                            <label class="pull-right mb-0" for="edo-ani">
                              <input class="radio_animated" id="edo-ani" type="radio" name="rdo-ani">
                            </label>
                          </td>
                        </tr>
                        <tr>
                          <td><img class="img-radius img-25 align-top m-r-15 rounded-circle" src="../../assets/images/university/math-2.jpg" alt="">
                            <div class="professor-block d-inline-block">Elan hormas
                              <p>Bio Professors</p>
                            </div>
                          </td>
                          <td>
                            <label class="pull-right mb-0" for="edo-ani1">
                              <input class="radio_animated" id="edo-ani1" type="radio" name="rdo-ani" checked="">
                            </label>
                          </td>
                        </tr>
                      </tbody>
                    </table>
                  </div>
                </div>
              </div>
            </div>
            <div class="col-md-6">
              <div class="card">
                <div class="card-header">
                  <h5>Bio Professors</h5>
                </div>
                <div class="card-body">
                  <div class="table-responsive professor-table mb-0">
                    <table class="table table-bordernone">
                      <tbody>
                        <tr>
                          <td><img class="img-radius img-25 align-top m-r-15 rounded-circle" src="../../assets/images/university/bio-1.jpg" alt="">
                            <div class="professor-block d-inline-block">Erana siddy
                              <p>Director</p>
                            </div>
                          </td>
                          <td>
                            <label class="pull-right mb-0" for="edo-ani2">
                              <input class="radio_animated" id="edo-ani2" type="radio" name="rdo-ani1" checked="">
                            </label>
                          </td>
                        </tr>
                        <tr>
                          <td><img class="img-radius img-35 align-top m-r-15 rounded-circle" src="../../assets/images/university/bio-2.jpg" alt="">
                            <div class="professor-block d-inline-block">Tom kerrly
                              <p>Director</p>
                            </div>
                          </td>
                          <td>
                            <label class="pull-right mb-0" for="edo-ani3">
                              <input class="radio_animated" id="edo-ani3" type="radio" name="rdo-ani1">
                            </label>
                          </td>
                        </tr>
                      </tbody>
                    </table>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="col-xl-4 xl-50">
          <div class="card height-equal">
            <div class="card-header">
              <h5>Upcoming Event</h5>
            </div>
            <div class="card-body">
              <div class="upcoming-event">
                <div class="upcoming-innner media">
                  <div class="bg-primary left m-r-20"><feather type="help-circle"></feather></div>
                  <div class="media-body">
                    <p class="mb-0">Demo Content <span class="pull-right">Mar 18</span></p>
                    <h6 class="f-w-600">Quiz Compition</h6>
                    <p class="mb-0">Lorem Ipsum is simply dummy text of the printing and typesetting industry. lorem ipsum</p>
                  </div>
                </div>
                <div class="upcoming-innner media">
                  <div class="bg-primary left m-r-20"><feather type="mic"></feather></div>
                  <div class="media-body">
                    <p class="mb-0">Demo Content <span class="pull-right">Sep 18</span></p>
                    <h6 class="f-w-600">Singing Compition</h6>
                    <p class="mb-0">Lorem Ipsum is simply dummy text of the printing and typesetting industry. lorem ipsum</p>
                  </div>
                </div>
                <div class="upcoming-innner media">
                  <div class="bg-primary left m-r-20"><feather type="zap"></feather></div>
                  <div class="media-body">
                    <p class="mb-0">Demo Content <span class="pull-right">Dec 18</span></p>
                    <h6 class="f-w-600">Diwali Celebration</h6>
                    <p class="mb-0">Lorem Ipsum is simply dummy text of the printing and typesetting industry. lorem ipsum</p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="col-xl-4 xl-50">
          <div class="card height-equal" data-intro="This is Ranker Ratio">
            <div class="card-header">
              <h5>Ranker Ratio</h5>
            </div>
            <div class="card-body">
              <div class="knob-block text-center knob-sm">
                <div class="knob" id="profit"></div>
              </div>
              <div class="ranker text-center">
                <h6>Student</h6>
                <h5 class="mb-0">New Ranker 2018</h5>
              </div>
            </div>
          </div>
        </div>

        <div class="col-xl-4 xl-100">
          <div class="card height-equal">
            <div class="card-header">
              <h5>Notification</h5>
            </div>
            <div class="card-body">
              <div class="notifiaction-media">
                <div class="media">
                  <div class="media-body">
                    <div class="circle-left"></div>
                    <h6>You are confirmation visit..<span class="pull-right f-12">1 Day Ago</span></h6>
                  </div>
                </div>
                <div class="media">
                  <div class="media-body">
                    <div class="circle-left"></div>
                    <h6>Lorem Ipsum has been the..<span class="pull-right f-12">5 Day Ago</span></h6>
                  </div>
                </div>
                <div class="media">
                  <div class="media-body">
                    <div class="circle-left"></div>
                    <h6>Standard dummy text ever..<span class="pull-right f-12">7 Day Ago</span></h6>
                  </div>
                </div>
                <div class="media">
                  <div class="media-body">
                    <div class="circle-left"></div>
                    <h6>When an unknown printer..<span class="pull-right f-12">9 Day Ago</span></h6>
                  </div>
                </div>
                <div class="media">
                  <div class="media-body">
                    <div class="circle-left"></div>
                    <h6>Took a gallery of type..<span class="pull-right f-12">6 Day Ago</span></h6>
                  </div>
                </div>
                <div class="media mb-0">
                  <div class="media-body">
                    <div class="circle-left"></div>
                    <h6>Scrambled it to make a type..<span class="pull-right f-12">2 Day Ago</span></h6>
                  </div>
                </div>
              </div>
            </div>
            <div class="card-footer btn-more text-center"><a href="#">MORE...</a></div>
          </div>
        </div>

        <div class="col-xl-6">
          <div class="card">
            <div class="card-header">
              <div class="row">
                <div class="col-sm-6">
                  <h5>Statistics</h5>
                  <button class="btn btn-primary btn-sm header-btn btn-pill">2017</button>
                </div>
                <div class="col-sm-6">
                  <div class="pull-right statistics">
                    <h5 class="counter">85</h5>
                    <p class="f-12 mb-0">Statistics 2017</p>
                    <div class="font-primary font-weight-bold d-flex f-11 pull-right"><i class="fa fa-sort-up mr-2"></i><span class="number"><span class="counter">100</span>%</span></div>
                  </div>
                </div>
              </div>
            </div>
            <div class="card-body">
              <div class="curves-2">
                <div class="animate-curve2 ct-golden-section">
                  <chartist
                  type="Line"
                  :data="animate_curve_chart2.chartData"
                  :options="animate_curve_chart2.chartOptions"/>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="col-xl-6">
          <div class="card">
            <div class="card-header">
              <div class="row">
                <div class="col-sm-6">
                  <h5>Last 5 Year Board</h5>
                  <p class="f-12 header-small mb-0">18 september, 2018</p>
                </div>
                <div class="col-sm-6">
                  <div class="pull-right statistics">
                    <h5 class="counter">50</h5>
                    <p class="f-12 mb-0">Board 2018</p>
                    <div class="font-primary font-weight-bold d-flex f-11 pull-right"><i class="fa fa-sort-up mr-2"></i><span class="number"><span class="counter">78</span>%</span></div>
                  </div>
                </div>
              </div>
            </div>
            <div class="card-body">
              <div class="animate-curve2 ct-golden-section">
                <chartist
                ratio="ct-major-second"
                type="Bar"
                :data="barchart.data"
                :options="barchart.options" />
              </div>
            </div>
          </div>
        </div>

        <div class="col-xl-8 xl-50">
          <div class="card" data-intro="This is Our Topper List">
            <div class="card-header">
              <h5>Our Topper List</h5>
            </div>
            <div class="card-body">
              <div class="table-responsive topper-lists mb-0">
                <table class="table table-bordernone">
                  <tbody>
                    <tr>
                      <td>
                        <div class="d-inline-block align-self-center">
                          <div class="form-group d-inline-block">
                            <div class="checkbox">
                              <input id="checkbox1" type="checkbox">
                              <label for="checkbox1"></label>
                            </div>
                          </div><img class="img-radius img-40 align-top m-r-15 rounded-circle" src="../../assets/images/user/4.jpg" alt="">
                          <div class="d-inline-block"><span class="f-w-600">Ossim Keter</span>
                            <p>1<sup>st</sup> year</p>
                          </div>
                        </div>
                      </td>
                      <td>
                        <div class="d-inline-block text-center"><span class="f-w-600">+48 605 562 215</span>
                          <p>Phone Number</p>
                        </div>
                      </td>
                      <td><img class="align-top" src="../../assets/images/university/chart-1.png" alt=""></td>
                      <td>
                        <div class="d-inline-block text-center"><span class="f-w-600">1</span>
                          <p>Rank</p>
                        </div>
                      </td>
                      <td>
                        <div class="d-inline-block text-center"><span class="f-w-600">590/600</span>
                          <p>Total marks</p>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td>
                        <div class="d-inline-block align-self-center">
                          <div class="form-group d-inline-block">
                            <div class="checkbox">
                              <input id="checkbox2" type="checkbox" checked="">
                              <label for="checkbox2"></label>
                            </div>
                          </div><img class="img-radius img-40 align-top m-r-15 rounded-circle" src="../../assets/images/university/math-1.jpg" alt="">
                          <div class="check-dot d-inline-block"></div>
                          <div class="d-inline-block"><span class="f-w-600">Venter Loren</span>
                            <p>1<sup>st</sup> year</p>
                          </div>
                        </div>
                      </td>
                      <td>
                        <div class="d-inline-block text-center"><span class="f-w-600">+25 598 559 368</span>
                          <p>Phone Number</p>
                        </div>
                      </td>
                      <td><img class="align-top" src="../../assets/images/university/chart-2.png" alt=""></td>
                      <td>
                        <div class="d-inline-block text-center"><span class="f-w-600">2</span>
                          <p>Rank</p>
                        </div>
                      </td>
                      <td>
                        <div class="d-inline-block text-center"><span class="f-w-600">570/600</span>
                          <p>Total marks</p>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td>
                        <div class="d-inline-block align-self-center">
                          <div class="form-group d-inline-block">
                            <div class="checkbox">
                              <input id="checkbox3" type="checkbox">
                              <label for="checkbox3"></label>
                            </div>
                          </div><img class="img-radius img-40 align-top m-r-15 rounded-circle" src="../../assets/images/user/2.png" alt="">
                          <div class="d-inline-block"><span class="f-w-600">Fran Loain</span>
                            <p>1<sup>st</sup> year</p>
                          </div>
                        </div>
                      </td>
                      <td>
                        <div class="d-inline-block text-center"><span class="f-w-600">+65 659 145 235</span>
                          <p>Phone Number</p>
                        </div>
                      </td>
                      <td><img class="align-top" src="../../assets/images/university/chart-3.png" alt=""></td>
                      <td>
                        <div class="d-inline-block text-center"><span class="f-w-600">3</span>
                          <p>Rank</p>
                        </div>
                      </td>
                      <td>
                        <div class="d-inline-block text-center"><span class="f-w-600">565/600</span>
                          <p>Total marks</p>
                        </div>
                      </td>
                    </tr>
                    <tr>
                      <td>
                        <div class="d-inline-block align-self-center">
                          <div class="form-group d-inline-block">
                            <div class="checkbox">
                              <input id="checkbox4" type="checkbox">
                              <label for="checkbox4"></label>
                            </div>
                          </div><img class="img-radius img-40 align-top m-r-15 rounded-circle" src="../../assets/images/user/5.jpg" alt="">
                          <div class="d-inline-block"><span class="f-w-600">Loften Horen</span>
                            <p>1<sup>st</sup> year</p>
                          </div>
                        </div>
                      </td>
                      <td>
                        <div class="d-inline-block text-center"><span class="f-w-600">+37 595 367 368</span>
                          <p>Phone Number</p>
                        </div>
                      </td>
                      <td><img class="align-top" src="../../assets/images/university/chart-4.png" alt=""></td>
                      <td>
                        <div class="d-inline-block text-center"><span class="f-w-600">4</span>
                          <p>Rank</p>
                        </div>
                      </td>
                      <td>
                        <div class="d-inline-block text-center"><span class="f-w-600">540/600</span>
                          <p>Total marks</p>
                        </div>
                      </td>
                    </tr>
                  </tbody>
                </table>
              </div>
            </div>
          </div>
        </div>

        <div class="col-xl-4 xl-50">
          <div class="card card-gradient">
            <div class="card-body text-center o-hidden">
              <div class="knob-header">
                <h5>Total Student</h5>
                <div class="d-inline-block pull-right f-16">120 / <span>130</span></div>
              </div>
              <div class="knob-block text-center knob-center">

                <div class="knob" id="total_students"></div>

              </div><img class="round-image" src="../../assets/images/university/round.png" alt="">
            </div>
          </div>
        </div>

               <div class="col-xl-4 xl-50">
                <div class="card" data-intro="This is Date picker">
                  <div class="datepicker-here date-picker-university" data-language="en">
                    <datepicker :inline="true"></datepicker>
                  </div>
                </div>
              </div>

              <div class="col-xl-8 xl-50">
                <div class="card">
                  <div class="card-header">
                    <h5>Admission Ratio</h5>
                  </div>
                  <div class="card-body chart-block admission-chart">
                    <Admission id="myLineCharts"/>
                  </div>
                </div>
              </div>

            </div>
          </div>
          <!-- Container-fluid Ends-->
        </div>
      </template>

      <script>
      import Admission from './chartjs/admissionchart'
      import Datepicker from 'vuejs-datepicker';
var primary = localStorage.getItem('primary_color') || '#4466f2';
      var Knob = require('knob')
      var profit = Knob({
        value: 35,
        angleOffset: -125,
        angleArc: 250,
        className: "review",
        lineCap: "round",
        thickness: 0.2,
        width: 295,
        height: 295,
        fgColor: primary,
      })

      var total_students = Knob({
        value: 85,
        angleOffset: 90,
        className: "review",
        lineCap: "round",
        thickness: 0.1,
        width: 180,
        height: 180,
        fgColor:'#fff',
        bgColor: primary
      })

      export default {
        data()
        {
          return{
            animate_curve_chart: {
              chartData: {
                labels: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul','Aug'],
                series: [
                [2, 3, 2.5, 5, 1.5, 4.5, 3, 3.1],
                [3, 3.5, 6, 1.1, 5, 2.5, 3.2, 2]
                ]
              },
              chartOptions: {
                low: 0,
                showPoint: false,
                chartPadding: {
                  left: -20,
                  right: 0,
                  bottom: 0,
                },
                axisY: {
                  scaleMinSpace: 40
                }
              }
            },
            animate_curve_chart2: {
              chartData: {
                labels: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul','Aug', 'Sep'],
                series: [
                [1.5, 3, 2, 1, 4, 1, 4, 2, 3, 2.5],
                [5, 4.7, 4, 3, 3.3, 3.7, 3, 3.8, 3, 2]
                ]
              },
              chartOptions: {
                low: 0,
                showPoint: false,
                chartPadding: {
                  left: -10,
                  right: 0,
                  bottom: -13,
                },
                axisY: {
                  scaleMinSpace: 40
                }
              }
            },
            barchart : {
              data: {
                labels: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug'],
                series: [
                [1, 2, 1.5, 3, 1.5, 0.8, 1.5, 2],
                [6, 4, 5, 6.5, 3, 2, 5.5, 7]
                ]
              },
              options: {
                seriesBarDistance: 12,
                chartPadding: {
                  left: -10,
                  right: 0,
                  bottom: -15
                },
                axisX: {
                  showGrid: false,
                  labelInterpolationFnc: function(value) {
                   return value[0];
                 }
               }
             },
           },
           widgetBar : {
              data: {
                labels: ['Q1', 'Q2', 'Q3', 'Q4', 'Q5', 'Q6'],
                series: [
                  [50, 200, 150, 400, 300, 600, 700]
                ]
              },
              options: {
                stackBars: true,
                axisY: {
                  low: 0,
                  showGrid: false,
                  showLabel: false,
                  offset: 0
                },
                axisX: {
                  showGrid: false,
                  showLabel: false,
                  offset: 0
                }
             },
             eventHandlers : [{
                event: 'draw',
                fn(data) {
                  if(data.type === 'bar') {
                    data.element.attr({
                      style: 'stroke-width: 2px'
                    });
                  } 
                }
              }]
            },
          }
       },
       components: {
        Datepicker,
        Admission
      },
      mounted () {
        document.getElementById('profit').append(profit),
        document.getElementById('total_students').append(total_students)
      }
    }
    </script>
