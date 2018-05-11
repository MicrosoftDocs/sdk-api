---
UID: NF:mfapi.MFGetAttributesAsBlob
title: MFGetAttributesAsBlob function
author: windows-driver-content
description: Converts the contents of an attribute store to a byte array.
old-location: mf\mfgetattributesasblob.htm
old-project: medfound
ms.assetid: 1a3bd860-1022-481f-8615-5a73c16dd77b
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: 1a3bd860-1022-481f-8615-5a73c16dd77b, MFGetAttributesAsBlob, MFGetAttributesAsBlob function [Media Foundation], mf.mfgetattributesasblob, mfapi/MFGetAttributesAsBlob
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_CUSTOM_DECODE_UNIT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mfplat.dll
api_name:
-	MFGetAttributesAsBlob
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFGetAttributesAsBlob function


## -description



Converts the contents of an attribute store to a byte array.




## -parameters




### -param pAttributes [in]

Pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface of the attribute store.


### -param pBuf [out]

Pointer to an array that receives the attribute data.


### -param cbBufSize [in]

Size of the <i>pBuf</i> array, in bytes. To get the required size of the buffer, call <a href="https://msdn.microsoft.com/52abfe30-a18d-45f7-93db-13f87b0647b7">MFGetAttributesAsBlobSize</a>.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The buffer given in <i>pBuf</i> is too small.

</td>
</tr>
</table>
 




## -remarks



The function skips any attributes with <b>IUnknown</b> pointer values (MF_ATTRIBUTE_IUNKNOWN); they are not stored in the array.

To convert the byte array back into an attribute store, call <a href="https://msdn.microsoft.com/da0f01a3-ed47-42a1-b4af-5f3cbc9271a3">MFInitAttributesFromBlob</a>.

To write an attribute store to a stream, call the <a href="https://msdn.microsoft.com/b8bc88e5-19ae-46b3-aa78-a00afee1f481">MFSerializeAttributesToStream</a> function.




## -see-also




<a href="https://msdn.microsoft.com/44af5e03-5f0a-4564-b9d6-b8c935df35b2">Attributes and Properties</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

