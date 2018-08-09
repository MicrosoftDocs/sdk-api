---
UID: NF:wmcontainer.MFCreateASFIndexer
title: MFCreateASFIndexer function
author: windows-sdk-content
description: Creates the ASF Indexer object.
old-location: mf\mfcreateasfindexer.htm
old-project: medfound
ms.assetid: df141f8e-10b4-4ac4-8a83-c25764b8f0c6
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: MFCreateASFIndexer, MFCreateASFIndexer function [Media Foundation], df141f8e-10b4-4ac4-8a83-c25764b8f0c6, mf.mfcreateasfindexer, wmcontainer/MFCreateASFIndexer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wmcontainer.h
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
req.typenames: MFSINK_WMDRMACTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateASFIndexer
product: Windows
targetos: Windows
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# MFCreateASFIndexer function


## -description



Creates the ASF Indexer object.




## -parameters




### -param ppIIndexer

Receives a pointer to the <a href="https://msdn.microsoft.com/93127fe4-bca9-4674-ae21-012367d7dd2f">IMFASFIndexer</a> interface. The caller must release the interface.


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
 

 

