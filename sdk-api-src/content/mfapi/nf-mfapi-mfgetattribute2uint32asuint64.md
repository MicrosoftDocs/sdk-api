---
UID: NF:mfapi.MFGetAttribute2UINT32asUINT64
title: MFGetAttribute2UINT32asUINT64 function (mfapi.h)
author: windows-sdk-content
description: Gets an attribute whose value is two UINT32 values packed into a UINT64.
old-location: mf\mfgetattribute2uint32asuint64.htm
tech.root: medfound
ms.assetid: 2b3050da-6914-4d7f-af6f-d8e504da0870
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MFGetAttribute2UINT32asUINT64, MFGetAttribute2UINT32asUINT64 function [Media Foundation], mf.mfgetattribute2uint32asuint64, mfobjects/MFGetAttribute2UINT32asUINT64
ms.topic: function
req.header: mfapi.h
req.include-header: Mfapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - mfobjects.h
api_name:
 - MFGetAttribute2UINT32asUINT64
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFGetAttribute2UINT32asUINT64 function


## -description


Gets an attribute whose value is two <b>UINT32</b> values packed into a <b>UINT64</b>.


## -parameters




### -param pAttributes [in]

A pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface of the attribute store.




### -param guidKey [in]

A <b>GUID</b> that identifies which value to retrieve. The attribute type must be <b>MF_ATTRIBUTE_UINT64</b>.


### -param punHigh32 [out]

Receives the high-order 32 bits.




### -param punLow32 [out]

Receives the low-order 32 bits.


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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_ATTRIBUTENOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified key was not found.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDTYPE</b></dt>
</dl>
</td>
<td width="60%">
The attribute value is not a <b>UINT64</b>.
              

</td>
</tr>
</table>
 




## -remarks



Internally, this function calls <a href="https://msdn.microsoft.com/f3240fff-48d8-4d88-8c75-15f00bfe72ed">IMFAttributes::GetUINT64</a> to get the <b>UINT64</b> value, and <a href="https://msdn.microsoft.com/507504c2-85d3-44b6-9972-bcdd3c4227f6">Unpack2UINT32AsUINT64</a> to unpack the two 32-bit values.




## -see-also




<a href="https://msdn.microsoft.com/44af5e03-5f0a-4564-b9d6-b8c935df35b2">Attributes and Properties</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

