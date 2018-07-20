---
UID: NF:mfapi.MFGetAttributesAsBlobSize
title: MFGetAttributesAsBlobSize function
author: windows-sdk-content
description: Retrieves the size of the buffer needed for the MFGetAttributesAsBlob function.
old-location: mf\mfgetattributesasblobsize.htm
old-project: medfound
ms.assetid: 52abfe30-a18d-45f7-93db-13f87b0647b7
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: 52abfe30-a18d-45f7-93db-13f87b0647b7, MFGetAttributesAsBlobSize, MFGetAttributesAsBlobSize function [Media Foundation], mf.mfgetattributesasblobsize, mfapi/MFGetAttributesAsBlobSize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mfapi.h
req.include-header: 
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
tech.root: 
req.typenames: MF_CUSTOM_DECODE_UNIT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFGetAttributesAsBlobSize
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFGetAttributesAsBlobSize function


## -description



Retrieves the size of the buffer needed for the <a href="https://msdn.microsoft.com/1a3bd860-1022-481f-8615-5a73c16dd77b">MFGetAttributesAsBlob</a> function.




## -parameters




### -param pAttributes [in]

Pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface of the attribute store.


### -param pcbBufSize [out]

Receives the required size of the array, in bytes.


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
</table>
 




## -remarks



Use this function to find the size of the array that is needed for the <a href="https://msdn.microsoft.com/1a3bd860-1022-481f-8615-5a73c16dd77b">MFGetAttributesAsBlob</a> function.




## -see-also




<a href="https://msdn.microsoft.com/44af5e03-5f0a-4564-b9d6-b8c935df35b2">Attributes and Properties</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

