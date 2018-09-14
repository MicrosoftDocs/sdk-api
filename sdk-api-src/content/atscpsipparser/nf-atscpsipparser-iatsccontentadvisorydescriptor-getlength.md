---
UID: NF:atscpsipparser.IAtscContentAdvisoryDescriptor.GetLength
title: IAtscContentAdvisoryDescriptor::GetLength
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatsccontentadvisorydescriptor_getlength.htm
tech.root: MSTV
ms.assetid: 954d7dc4-43dd-4e33-a3cf-7584092cd0e7
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetLength, GetLength method [Microsoft TV Technologies], GetLength method [Microsoft TV Technologies],IAtscContentAdvisoryDescriptor interface, IAtscContentAdvisoryDescriptor interface [Microsoft TV Technologies],GetLength method, IAtscContentAdvisoryDescriptor.GetLength, IAtscContentAdvisoryDescriptor::GetLength, IAtscContentAdvisoryDescriptorGetLength, atscpsipparser/IAtscContentAdvisoryDescriptor::GetLength, mstv.iatsccontentadvisorydescriptor_getlength
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: atscpsipparser.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - IAtscContentAdvisoryDescriptor.GetLength
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAtscContentAdvisoryDescriptor::GetLength


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetLength</b> method returns the length of the descriptor body.


## -parameters




### -param pbVal [out]

Receives the length of the descriptor body, in bytes.


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




<a href="https://msdn.microsoft.com/b7379d66-c57b-45e0-9c63-901bf3637f21">IAtscContentAdvisoryDescriptor Interface</a>
 

 

