---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IWMPEvents::KeyDown


## -description



The <b>KeyDown</b> event occurs when a key is pressed.




## -parameters




### -param nKeyCode [in]

Specifies which physical key is pressed. For possible values, see the Remarks section.


### -param nShiftState [in]

A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2). These bits correspond to the values 1, 2, and 4, respectively. The shift argument indicates the state of these keys. Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.


## -returns



This method does not return a value.




## -remarks



The <i>nKeyCode</i> argument specifies a physical key. The following tables show the possible values for the major keys on a standard keyboard.

Values for the main keys.

<table>
<tr>
<th>
              Key
            </th>
<th>
              Value
            </th>
</tr>
<tr>
<td>A-Z</td>
<td>65-90</td>
</tr>
<tr>
<td>0-9</td>
<td>48-56</td>
</tr>
<tr>
<td>F1-F12</td>
<td>112-123</td>
</tr>
<tr>
<td>ESC</td>
<td>27</td>
</tr>
<tr>
<td>TAB</td>
<td>9</td>
</tr>
<tr>
<td>CAPS LOCK</td>
<td>20</td>
</tr>
<tr>
<td>SHIFT (left or right)</td>
<td>16</td>
</tr>
<tr>
<td>CTRL (left or right)</td>
<td>17</td>
</tr>
<tr>
<td>ALT (left or right)</td>
<td>18</td>
</tr>
<tr>
<td>SPACE</td>
<td>32</td>
</tr>
<tr>
<td>BACKSPACE</td>
<td>8</td>
</tr>
<tr>
<td>ENTER</td>
<td>13</td>
</tr>
<tr>
<td>Windows logo key, left</td>
<td>91</td>
</tr>
<tr>
<td>Windows logo key, right</td>
<td>92</td>
</tr>
<tr>
<td>Application key</td>
<td>93</td>
</tr>
</table>
 

Values for the number pad keys.

<table>
<tr>
<th>
              Key
            </th>
<th>
              Value
            </th>
</tr>
<tr>
<td>0-9</td>
<td>96-105</td>
</tr>
<tr>
<td>NUM LOCK</td>
<td>144</td>
</tr>
<tr>
<td>DIVIDE (/)</td>
<td>111</td>
</tr>
<tr>
<td>MULTIPLY (*)</td>
<td>106</td>
</tr>
<tr>
<td>SUBTRACT (-)</td>
<td>109</td>
</tr>
<tr>
<td>ADD (+)</td>
<td>107</td>
</tr>
<tr>
<td>SEPARATOR (Enter)</td>
<td>108</td>
</tr>
<tr>
<td>DECIMAL (.)</td>
<td>110</td>
</tr>
</table>
 

Values for the navigation keys.

<table>
<tr>
<th>
              Key
            </th>
<th>
              Value
            </th>
</tr>
<tr>
<td>INSERT</td>
<td>45</td>
</tr>
<tr>
<td>DELETE</td>
<td>46</td>
</tr>
<tr>
<td>HOME</td>
<td>36</td>
</tr>
<tr>
<td>END</td>
<td>35</td>
</tr>
<tr>
<td>PAGE UP</td>
<td>33</td>
</tr>
<tr>
<td>PAGE DOWN</td>
<td>34</td>
</tr>
<tr>
<td>UP ARROW</td>
<td>38</td>
</tr>
<tr>
<td>DOWN ARROW</td>
<td>40</td>
</tr>
<tr>
<td>LEFT ARROW</td>
<td>37</td>
</tr>
<tr>
<td>RIGHT ARROW</td>
<td>39</td>
</tr>
</table>
 

<b>Windows Media Player 10 Mobile: </b>This event is not supported.




## -see-also




<a href="https://msdn.microsoft.com/396545d5-8844-4dd2-9ed5-e4ed77f352ac">IWMPEvents Interface</a>
 

 

