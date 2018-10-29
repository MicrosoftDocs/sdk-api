---
UID: NF:msinkaut.IInkDisp.CanPaste
title: IInkDisp::CanPaste
author: windows-sdk-content
description: Indicates whether the IDataObject can be converted to an InkDisp object.
old-location: tablet\inkdisp_canpaste.htm
tech.root: tablet
ms.assetid: 755c74c4-417a-49b5-9f3d-9348c05ac850
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: 755c74c4-417a-49b5-9f3d-9348c05ac850, CanPaste, CanPaste method [Tablet PC], CanPaste method [Tablet PC],IInkDisp interface, IInkDisp interface [Tablet PC],CanPaste method, IInkDisp.CanPaste, IInkDisp::CanPaste, msinkaut/IInkDisp::CanPaste, tablet.inkdisp_canpaste
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkDisp.CanPaste
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkDisp::CanPaste


## -description



Indicates whether the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> can be converted to an <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object.




## -parameters




### -param DataObject [in, optional]

Optional. Specifies the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> to inspect. The default value is <b>NULL</b>, which means the data object on the Clipboard is used.


### -param CanPaste [out, retval]

<b>VARIANT_TRUE</b> if the data object can be converted to an <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object; otherwise, <b>VARIANT_FALSE</b>.


## -returns



This method can return one of these values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter contained an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
</table>
 




## -remarks



If the supplied <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> is <b>NULL</b>, then the data object on the Clipboard is used.




## -see-also




<a href="https://msdn.microsoft.com/85B683AA-D859-4717-8C61-C0EB4BBA5F61">IInkDisp</a>



<a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp Class</a>
 

 

