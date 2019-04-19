---
UID: NF:d2d1_1.ID2D1Effect.SetInputCount
title: ID2D1Effect::SetInputCount (d2d1_1.h)
author: windows-sdk-content
description: Allows the application to change the number of inputs to an effect.
old-location: direct2d\id2d1effect_setnumberofinputs.htm
tech.root: Direct2D
ms.assetid: cdcaa997-acbe-40e3-9439-629b3853d8d4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID2D1Effect interface [Direct2D],SetInputCount method, ID2D1Effect.SetInputCount, ID2D1Effect::SetInputCount, SetInputCount, SetInputCount method [Direct2D], SetInputCount method [Direct2D],ID2D1Effect interface, d2d1_1/ID2D1Effect::SetInputCount, direct2d.id2d1effect_setnumberofinputs
ms.topic: method
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Effect.SetInputCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1Effect::SetInputCount


## -description


Allows the application to change the number of inputs to an effect.


## -parameters




### -param inputCount

Type: <b>UINT32</b>

The number of inputs to the effect.


## -returns



Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>No error occurred.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>One or more arguments are invalid.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>Failed to allocate necessary memory.</td>
</tr>
</table>
 




## -remarks



Most effects do not support a variable number of inputs. Use <a href="https://msdn.microsoft.com/01678e13-df23-47bb-9af7-9f2ecaf03577">ID2D1Properties::GetValue</a> with the <b>D2D1_PROPERTY_MIN_INPUTS</b> and <b>D2D1_PROPERTY_MAX_INPUTS</b> values to determine the number of inputs supported by an effect.

If the input count is less than the minimum or more than the maximum supported inputs, the call will fail.

If the input count is unchanged, the call will succeed with <b>S_OK</b>. 

Any inputs currently selected on the effect will be unaltered by this call unless the number of inputs is made smaller. If the number of inputs is made smaller, inputs beyond the selected range will be released.

If the method fails, the existing input and input count will remain unchanged.




## -see-also




<a href="https://msdn.microsoft.com/dfe587f9-e92f-4367-a503-edd446a91cb8">ID2D1DeviceContext::CreateEffect</a>



<a href="https://msdn.microsoft.com/c41d8a79-280a-451e-b07b-f904d07da5c7">ID2D1DeviceContext::DrawImage</a>



<a href="https://msdn.microsoft.com/e90d1830-c356-48f1-ac7b-1d94c8c26569">ID2D1Effect</a>



<a href="https://msdn.microsoft.com/e14066f7-b195-44f1-a952-1b6c9f3832cf">ID2D1Effect::GetOutput</a>



<a href="https://msdn.microsoft.com/9f7b4546-edbe-4000-a4ce-1a69563ebf9d">ID2D1Image</a>
 

 

