---
UID: NF:wmsdkidl.WMCreateIndexer
title: WMCreateIndexer function
author: windows-sdk-content
description: The WMCreateIndexer function creates an indexer object.
old-location: wmformat\wmcreateindexer.htm
old-project: wmformat
ms.assetid: 08f83923-ed33-41d2-b7f8-d70627197b31
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: WMCreateIndexer, WMCreateIndexer function [windows Media Format], wmformat.wmcreateindexer, wmsdkidl/WMCreateIndexer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wmvcore.dll
api_name:
-	WMCreateIndexer
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WMCreateIndexer function


## -description



The <b>WMCreateIndexer</b> function creates an indexer object.




## -parameters




### -param ppIndexer [out]

Pointer to a pointer to the <a href="https://msdn.microsoft.com/00627b0c-4484-417a-8680-0fd97aac41fe">IWMIndexer</a> interface of the newly created indexer object.


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
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The function is unable to allocate memory for the new object.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/00627b0c-4484-417a-8680-0fd97aac41fe">IWMIndexer Interface</a>



<a href="https://msdn.microsoft.com/652e04a5-ed6e-4e92-acf4-55ed82f77ef1">Indexer Object</a>
 

 

