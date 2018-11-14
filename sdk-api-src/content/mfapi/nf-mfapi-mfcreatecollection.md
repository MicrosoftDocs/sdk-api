---
UID: NF:mfapi.MFCreateCollection
title: MFCreateCollection function
author: windows-sdk-content
description: Creates an empty collection object.
old-location: mf\mfcreatecollection.htm
tech.root: medfound
ms.assetid: 6a7bf7b6-62f1-4eac-9849-39021ee50f42
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: 6a7bf7b6-62f1-4eac-9849-39021ee50f42, MFCreateCollection, MFCreateCollection function [Media Foundation], mf.mfcreatecollection, mfapi/MFCreateCollection
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreateCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- MFCreateCollection
: 
---

# MFCreateCollection function


## -description



Creates an empty collection object.




## -parameters




### -param ppIMFCollection [out]

Receives a pointer to the collection object's <a href="https://msdn.microsoft.com/fec6aa17-2770-4f53-b36d-b94236093d23">IMFCollection</a> interface. The caller must release the interface.


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
The method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

