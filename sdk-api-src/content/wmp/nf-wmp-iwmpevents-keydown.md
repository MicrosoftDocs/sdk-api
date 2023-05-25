---
UID: NF:wmp.IWMPEvents.KeyDown
title: IWMPEvents::KeyDown (wmp.h)
description: The KeyDown event occurs when a key is pressed.
helpviewer_keywords: ["IWMPEvents interface [Windows Media Player]","KeyDown method","IWMPEvents.KeyDown","IWMPEvents::KeyDown","IWMPEventsKeyDown","KeyDown","KeyDown method [Windows Media Player]","KeyDown method [Windows Media Player]","IWMPEvents interface","wmp.iwmpevents_iwmpevents__keydown","wmp/IWMPEvents::KeyDown"]
old-location: wmp\iwmpevents_iwmpevents__keydown.htm
tech.root: WMP
ms.assetid: 3759d40c-414a-4f91-93eb-0ad4a4b091b9
ms.date: 4/26/2023
ms.keywords: IWMPEvents interface [Windows Media Player],KeyDown method, IWMPEvents.KeyDown, IWMPEvents::KeyDown, IWMPEventsKeyDown, KeyDown, KeyDown method [Windows Media Player], KeyDown method [Windows Media Player],IWMPEvents interface, wmp.iwmpevents_iwmpevents__keydown, wmp/IWMPEvents::KeyDown
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
req.lib: 
req.dll: Wmp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPEvents::KeyDown
 - wmp/IWMPEvents::KeyDown
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPEvents.KeyDown
---

# IWMPEvents::KeyDown


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>KeyDown</b> event occurs when a key is pressed.

## -parameters

### -param nKeyCode [in]

Specifies which physical key is pressed. For possible values, see the Remarks section.

### -param nShiftState [in]

A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2). These bits correspond to the values 1, 2, and 4, respectively. The shift argument indicates the state of these keys. Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.

## -remarks

The <i>nKeyCode</i> argument specifies a physical key. The following tables show the possible values for the major keys on a standard keyboard.

Values for the main keys.

<table>
<tr>
<th>Key
            </th>
<th>Value
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
<th>Key
            </th>
<th>Value
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
<th>Key
            </th>
<th>Value
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

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents">IWMPEvents Interface</a>