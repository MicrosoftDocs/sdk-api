---
UID: NF:segment.IMSVidVMR9.SetAllocator
title: IMSVidVMR9::SetAllocator
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
old-location: mstv\imsvidvmr9_setallocator.htm
tech.root: MSTV
ms.assetid: f654adac-12b6-47c7-99d4-0612b1532df4
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IMSVidVMR9 interface [Microsoft TV Technologies],SetAllocator method, IMSVidVMR9.SetAllocator, IMSVidVMR9::SetAllocator, IMSVidVMR9SetAllocator, SetAllocator, SetAllocator method [Microsoft TV Technologies], SetAllocator method [Microsoft TV Technologies],IMSVidVMR9 interface, mstv.imsvidvmr9_setallocator, segment/IMSVidVMR9::SetAllocator
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
 - IMSVidVMR9.SetAllocator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidVMR9::SetAllocator


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>SetAllocator</b> method sets a custom allocator-presenter for the VMR-9.


## -parameters




### -param AllocPresent [in]

Pointer to the <b>IUnknown</b> interface of the allocator-presenter. This object must expose the <a href="https://msdn.microsoft.com/dd187168-19c7-414c-a764-f180d1d310f2">IVMRSurfaceAllocator9</a> interface. To use the VMR-9 filter's default allocator-presenter, set this parameter to <b>NULL</b>.


### -param ID [in]

Application-defined identifier for the allocator-presenter.


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
 




## -see-also




<a href="https://msdn.microsoft.com/c96f91d4-fc6c-4422-8fc9-ea5fed10bd80">IMSVidVMR9 Interface</a>
 

 

