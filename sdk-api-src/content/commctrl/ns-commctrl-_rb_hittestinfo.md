---
UID: NS:commctrl._RB_HITTESTINFO
title: "_RB_HITTESTINFO"
author: windows-sdk-content
description: Contains information specific to a hit test operation. This structure is used with the RB_HITTEST message.
old-location: controls\RBHITTESTINFO.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\rebar\structures\rbhittestinfo.htm
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: "*LPRBHITTESTINFO, LPRBHITTESTINFO, LPRBHITTESTINFO structure pointer [Windows Controls], RBHITTESTINFO, RBHITTESTINFO structure [Windows Controls], RBHT_CAPTION, RBHT_CHEVRON, RBHT_CLIENT, RBHT_GRABBER, RBHT_NOWHERE, RBHT_SPLITTER, _RB_HITTESTINFO, _win32_RBHITTESTINFO, _win32_RBHITTESTINFO_cpp, commctrl/LPRBHITTESTINFO, commctrl/RBHITTESTINFO, controls.RBHITTESTINFO, controls._win32_RBHITTESTINFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RBHITTESTINFO, *LPRBHITTESTINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	RBHITTESTINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _RB_HITTESTINFO structure


## -description


Contains information specific to a hit test operation. This structure is used with the <a href="https://msdn.microsoft.com/8f27db21-50d8-438f-a44c-2e65dd93fa2a">RB_HITTEST</a> message. 


## -struct-fields




### -field pt

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a></b>


<a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure that describes the point to be hit tested, in client coordinates. 


### -field flags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Member that receives a flag value indicating the rebar band's component located at the point described by <b>pt</b>. This member will be one of the following:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RBHT_CAPTION"></a><a id="rbht_caption"></a><dl>
<dt><b>RBHT_CAPTION</b></dt>
</dl>
</td>
<td width="60%">
The point was in the rebar band's caption.

</td>
</tr>
<tr>
<td width="40%"><a id="RBHT_CHEVRON"></a><a id="rbht_chevron"></a><dl>
<dt><b>RBHT_CHEVRON</b></dt>
</dl>
</td>
<td width="60%">
The point was in the rebar band's chevron (version 5.80 and greater).

</td>
</tr>
<tr>
<td width="40%"><a id="RBHT_CLIENT"></a><a id="rbht_client"></a><dl>
<dt><b>RBHT_CLIENT</b></dt>
</dl>
</td>
<td width="60%">
The point was in the rebar band's client area. 

</td>
</tr>
<tr>
<td width="40%"><a id="RBHT_GRABBER"></a><a id="rbht_grabber"></a><dl>
<dt><b>RBHT_GRABBER</b></dt>
</dl>
</td>
<td width="60%">
The point was in the rebar band's gripper. 

</td>
</tr>
<tr>
<td width="40%"><a id="RBHT_NOWHERE"></a><a id="rbht_nowhere"></a><dl>
<dt><b>RBHT_NOWHERE</b></dt>
</dl>
</td>
<td width="60%">
The point was not in a rebar band. 

</td>
</tr>
<tr>
<td width="40%"><a id="RBHT_SPLITTER"></a><a id="rbht_splitter"></a><dl>
<dt><b>RBHT_SPLITTER</b></dt>
</dl>
</td>
<td width="60%">
The point was in the rebar band's splitter.

</td>
</tr>
</table>
 


### -field iBand

Type: <b>int</b>

Member that receives the rebar band's index at the point described by <b>pt</b>. This value will be the zero-based index of the band, or -1 if no band was at the hit-tested point.

