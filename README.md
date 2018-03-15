# mi-prueba-perfecta-1
binary bot prueba perfecta 1 
  <block type="loader" id="G8*bH0yYOiK7:XhZ-!pX" x="0" y="0">
    <field name="URL">https://github.com/wilson2018prueba/mi-prueba-perfecta-1.git</field>
  </block>
  <block type="trade" id=")inu1KBx=?O=ZEkmjl_" x="0" y="-1"><"trade" id=")inu*9KBx=?O=ZEkmjl_" x="0" y="-19">
    <field name="MARKET_LIST">volidx</field>
    <field name="SUBMARKET_LIST">discontinous_index</field>
    <field name="SYMBOL_LIST">R_10</field>
    <field name="TRADETYPECAT_LIST">callput</field>
    <field name="TRADETYPE_LIST">risefall</field>
    <field name="TYPE_LIST">both</field>
    <field name="CANDLEINTERVAL_LIST">60</field>
    <field name="TIME_MACHINE_ENABLED">TRUE</field>
    <field name="RESTART">TRUE</field>
    <statement name="SUBMARKET">
      <block type="tradeOptions" id="pdY+@|R40e]2H`1uzIz9">
        <field name="DURATIONTYPE_LIST">t</field>
        <field name="CURRENCY_LIST">USD</field>
        <value name="DURATION">
          <block type="math_number" id="sxYl%U5{t^f,Mj-zA7M5">
            <field name="NUM">5</field>
          </block>
        </value>
        <value name="AMOUNT">
          <block type="procedures_callreturn" id="#4O1V{hS-`.=f(Vye8_">
            <mutation name="Martingale Trade Amount"></mutation>
          </block>
        </value>
      </block>
    </statement>
  </block>
  <block type="before_purchase" id="*Q[~K|v:Sg)bHrl+VA1N" x="0" y="-456">
    <statement name="BEFOREPURCHASE_STACK">
      <block type="purchase" id="Ot~~0{MHI(WEeSm{nTP4">
        <field name="PURCHASE_LIST">CALL</field>
      </block>
    </statement>
  </block>
  <block type="after_purchase" id="X[gun7Sx6Shn3kldC}mZ" x="0" y="456">
    <statement name="AFTERPURCHASE_STACK">
      <block type="controls_if" id="#=yO.C1rn7n]Zw*%E1AI">
        <value name="IF0">
          <block type="procedures_callreturn" id=")5H0+av/lasc#QI6to2^">
            <mutation name="Martingale Trade Again After Purchase">
              <arg name="martingale:profit"></arg>
              <arg name="martingale:resultIsWin"></arg>
            </mutation>
            <value name="ARG0">
              <block type="read_details" id="(E,!25pd^Ev`yMmr[z*_">
                <field name="DETAIL_INDEX">4</field>
              </block>
            </value>
            <value name="ARG1">
              <block type="contract_check_result" id="^ShXafO+N,gqVXtl^w)e">
                <field name="CHECK_RESULT">win</field>
              </block>
            </value>
          </block>
        </value>
        <statement name="DO0">
          <block type="trade_again" id=",vG2~pX|wvNj6hMyw=%~"></block>
        </statement>
      </block>
    </statement>
  </block>
</xml>
