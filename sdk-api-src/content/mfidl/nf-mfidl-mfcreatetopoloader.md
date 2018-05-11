---
UID: NF:mfidl.MFCreateTopoLoader
title: MFCreateTopoLoader function
author: windows-driver-content
description: Creates a new instance of the topology loader.
old-location: mf\mfcreatetopoloader.htm
old-project: medfound
ms.assetid: 0c0173ef-9c29-465c-b725-ce38b220f94f
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: 0c0173ef-9c29-465c-b725-ce38b220f94f, MFCreateTopoLoader, MFCreateTopoLoader function [Media Foundation], mf.mfcreatetopoloader, mfidl/MFCreateTopoLoader
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mf.dll
api_name:
-	MFCreateTopoLoader
product: Windows
targetos: Windows
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFCreateTopoLoader function


## -description



Creates a new instance of the topology loader.




## -parameters




### -param ppObj

Receives a pointer to the <a href="https://msdn.microsoft.com/5ebf117c-e60a-40f2-a24b-c4f9dbdae942">IMFTopoLoader</a> interface of the topology loader. The caller must release the interface.


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
 




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

