---
UID: NS:oledlg.tagOLEUIVIEWPROPSW
title: tagOLEUIVIEWPROPSW
author: windows-sdk-content
description: Contains information that is used to initialize the View tab of the Object properties dialog box.
old-location: com\oleuiviewprops_struct.htm
tech.root: com
ms.assetid: e45565c5-185e-4143-a5c2-d0b273b5086e
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*LPOLEUIVIEWPROPSW, *POLEUIVIEWPROPSW, LPOLEUIVIEWPROPS, LPOLEUIVIEWPROPS structure pointer [COM], OLEUIVIEWPROPS, OLEUIVIEWPROPS structure [COM], OLEUIVIEWPROPSA, OLEUIVIEWPROPSW, POLEUIVIEWPROPS, POLEUIVIEWPROPS structure pointer [COM], VPF_DISABLERELATIVE, VPF_DISABLESCALE, VPF_SELECTRELATIVE, _ole_OLEUIVIEWPROPS, com.oleuiviewprops_struct, oledlg/LPOLEUIVIEWPROPS, oledlg/OLEUIVIEWPROPS, oledlg/OLEUIVIEWPROPSA, oledlg/OLEUIVIEWPROPSW, oledlg/POLEUIVIEWPROPS, tagOLEUIVIEWPROPSW"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: oledlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OLEUIVIEWPROPSW (Unicode) and OLEUIVIEWPROPSA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OleDlg.h
api_name:
 - OLEUIVIEWPROPS
 - OLEUIVIEWPROPSA
 - OLEUIVIEWPROPSW
product: Windows
targetos: Windows
req.typenames: OLEUIVIEWPROPSW, *POLEUIVIEWPROPSW, *LPOLEUIVIEWPROPSW
req.redist: 
---

# tagOLEUIVIEWPROPSW structure


## -description


Contains information that is used to initialize the <b>View</b> tab of the <b>Object properties</b> dialog box. A reference to it is passed in as part of the <a href="https://msdn.microsoft.com/7a6216d6-061f-48c3-8e3f-5f3e5a63ffb3">OLEUIOBJECTPROPS</a> structure to the <a href="https://msdn.microsoft.com/591f6056-2e5f-4e58-8806-9a0093de2463">OleUIObjectProperties</a> function. This tab allows the user to toggle between "content" and "iconic" views of the object, and change its scaling within the container. It also allows the user to tunnel to the change icon dialog box when the object is being displayed iconically.


## -struct-fields




### -field cbStruct

The size of the structure, in bytes.


### -field dwFlags

Flags specific to view page.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VPF_SELECTRELATIVE"></a><a id="vpf_selectrelative"></a><dl>
<dt><b>VPF_SELECTRELATIVE</b></dt>
</dl>
</td>
<td width="60%">
Relative to origin.

</td>
</tr>
<tr>
<td width="40%"><a id="VPF_DISABLERELATIVE"></a><a id="vpf_disablerelative"></a><dl>
<dt><b>VPF_DISABLERELATIVE</b></dt>
</dl>
</td>
<td width="60%">
Disable relative to origin.

</td>
</tr>
<tr>
<td width="40%"><a id="VPF_DISABLESCALE"></a><a id="vpf_disablescale"></a><dl>
<dt><b>VPF_DISABLESCALE</b></dt>
</dl>
</td>
<td width="60%">
Disable scale option.

</td>
</tr>
</table>
 


### -field dwReserved1

This member is reserved.


### -field lpfnHook

Pointer to a hook callback (not used in this dialog box).


### -field lCustData

Custom data to pass to the hook (not used in this dialog box).


### -field dwReserved2

This member is reserved.


### -field lpOP

Used internally.


### -field nScaleMin

Minimum value for the scale range.


### -field nScaleMax

Maximum value for the scale range.



## -see-also




<a href="https://msdn.microsoft.com/7a6216d6-061f-48c3-8e3f-5f3e5a63ffb3">OLEUIOBJECTPROPS</a>
 

 

