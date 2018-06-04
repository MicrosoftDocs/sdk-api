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

# DrawThemeParentBackgroundEx function


## -description


Used by partially-transparent or alpha-blended child controls to draw the part of their parent in front of which they appear. Sends a <a href="https://msdn.microsoft.com/3bdc37da-227c-4be1-bf0b-99704b8acbe1">WM_ERASEBKGND</a> message followed by a <a href="https://msdn.microsoft.com/8703ee74-812a-4ca2-8ee3-a3b8779739e7">WM_PRINTCLIENT</a>.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle of the child control.


### -param hdc [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

HDC of the child control.


### -param dwFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Zero or more of the following values. If this value is zero, this function returns S_OK only if the parent handled <a href="https://msdn.microsoft.com/8703ee74-812a-4ca2-8ee3-a3b8779739e7">WM_PRINTCLIENT</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DTPB_WINDOWDC"></a><a id="dtpb_windowdc"></a><dl>
<dt><b>DTPB_WINDOWDC</b></dt>
</dl>
</td>
<td width="60%">
If set, <i>hdc</i> is assumed to be a window DC, not a client DC.

</td>
</tr>
<tr>
<td width="40%"><a id="DTPB_USECTLCOLORSTATIC"></a><a id="dtpb_usectlcolorstatic"></a><dl>
<dt><b>DTPB_USECTLCOLORSTATIC</b></dt>
</dl>
</td>
<td width="60%">
If set, this function sends a <a href="https://msdn.microsoft.com/a171a1e8-6845-4a8e-8394-44cea99d2b0d">WM_CTLCOLORSTATIC</a> message to the parent and uses the brush if one is provided. Otherwise, it uses COLOR_BTNFACE.

</td>
</tr>
<tr>
<td width="40%"><a id="DTPB_USEERASEBKGND"></a><a id="dtpb_useerasebkgnd"></a><dl>
<dt><b>DTPB_USEERASEBKGND</b></dt>
</dl>
</td>
<td width="60%">
If set, this function returns S_OK without sending a <a href="https://msdn.microsoft.com/a171a1e8-6845-4a8e-8394-44cea99d2b0d">WM_CTLCOLORSTATIC</a> message if the parent actually painted on <a href="https://msdn.microsoft.com/3bdc37da-227c-4be1-bf0b-99704b8acbe1">WM_ERASEBKGND</a>.

</td>
</tr>
</table>
 


### -param prc [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

Optional. The area to be drawn, in child coordinates. If this parameter is NULL, the area to be drawn includes the entire area occupied by the child control. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

S_OK if successful; otherwise, S_FALSE.



