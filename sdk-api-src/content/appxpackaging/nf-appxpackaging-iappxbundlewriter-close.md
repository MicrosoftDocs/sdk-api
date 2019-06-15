---
UID: NF:appxpackaging.IAppxBundleWriter.Close
title: IAppxBundleWriter::Close (appxpackaging.h)
author: windows-sdk-content
description: Finalizes the bundle package by writing footprint files at the end of the package, and closes the writer’s output stream.
old-location: appxpkg\iappxbundlewriter_close.htm
tech.root: appxpkg
ms.assetid: 9826873D-87AF-4D6B-977B-1C24197C47F8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Close, Close method [App packaging and management], Close method [App packaging and management],IAppxBundleWriter interface, IAppxBundleWriter interface [App packaging and management],Close method, IAppxBundleWriter.Close, IAppxBundleWriter::Close, appxpackaging/IAppxBundleWriter::Close, appxpkg.iappxbundlewriter_close
ms.topic: method
f1_keywords: ["appxpackaging/IAppxBundleWriter.Close"]
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: AppxPackaging.idl
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
 - AppxPackaging.h
api_name:
 - IAppxBundleWriter.Close
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxBundleWriter::Close


## -description


Finalizes the bundle package by writing footprint files at the end of the package, and closes the writer’s output stream.


## -parameters






## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code that includes, but is not limited to, those in the following table. 

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOT_VALID_STATE </b></dt>
</dl>
</td>
<td width="60%">
The writer is closed.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlewriter">IAppxBundleWriter</a>
 

 

