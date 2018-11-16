---
UID: NS:commctrl.tagREBARINFO
title: tagREBARINFO
author: windows-sdk-content
description: Contains information that describes rebar control characteristics.
old-location: controls\REBARINFO.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\rebar\structures\rebarinfo.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*LPREBARINFO, LPREBARINFO, LPREBARINFO structure pointer [Windows Controls], RBIM_IMAGELIST, REBARINFO, REBARINFO structure [Windows Controls], _win32_REBARINFO, _win32_REBARINFO_cpp, commctrl/LPREBARINFO, commctrl/REBARINFO, controls.REBARINFO, controls._win32_REBARINFO, tagREBARINFO"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - REBARINFO
product: Windows
targetos: Windows
req.typenames: REBARINFO, *LPREBARINFO
req.redist: 
---

# tagREBARINFO structure


## -description


Contains information that describes rebar control characteristics. 


## -struct-fields




### -field cbSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Size of this structure, in bytes. Your application must fill this member before sending any messages that use the address of this structure as a parameter. 


### -field fMask

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Flag values that describe characteristics of the rebar control. Currently, rebar controls support only one value: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RBIM_IMAGELIST"></a><a id="rbim_imagelist"></a><dl>
<dt><b>RBIM_IMAGELIST</b></dt>
</dl>
</td>
<td width="60%">
The 
						<b>himl</b> member is valid or must be filled. 

</td>
</tr>
</table>
 


### -field himl

Type: <b>HIMAGELIST</b>

Handle to an image list. The rebar control will use the specified image list to obtain images. 

