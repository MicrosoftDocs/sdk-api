---
UID: NF:segment.IMSVidVMR9.get_Allocator_ID
title: IMSVidVMR9::get_Allocator_ID
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
old-location: mstv\imsvidvmr9_get_allocator_id.htm
tech.root: mstv
ms.assetid: 46ea07af-be29-4621-96cb-f3c17be12f85
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMSVidVMR9 interface [Microsoft TV Technologies],get_Allocator_ID method, IMSVidVMR9.get_Allocator_ID, IMSVidVMR9::get_Allocator_ID, IMSVidVMR9get_Allocator_ID, get_Allocator_ID, get_Allocator_ID method [Microsoft TV Technologies], get_Allocator_ID method [Microsoft TV Technologies],IMSVidVMR9 interface, mstv.imsvidvmr9_get_allocator_id, segment/IMSVidVMR9::get_Allocator_ID
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidVMR9.get_Allocator_ID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidVMR9::get_Allocator_ID


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>get_Allocator_ID</b> method retrieves the identifier of the application's custom allocator-presenter.


## -parameters




### -param ID [out]

Receives the identifier. If the application did not set an allocator-presenter, the value is –1.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



To set a custom allocator-presenter, call <a href="https://msdn.microsoft.com/f654adac-12b6-47c7-99d4-0612b1532df4">IMSVidVMR9::SetAllocator</a>.




## -see-also




<a href="https://msdn.microsoft.com/c96f91d4-fc6c-4422-8fc9-ea5fed10bd80">IMSVidVMR9 Interface</a>
 

 

