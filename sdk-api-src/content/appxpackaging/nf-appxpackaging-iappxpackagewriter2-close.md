---
UID: NF:appxpackaging.IAppxPackageWriter2.Close
title: IAppxPackageWriter2::Close method
author: windows-driver-content
description: Closes the package writer object's output stream.
old-location: appxpkg\iappxpackagewriter2_close.htm
old-project: appxpkg
ms.assetid: C972B7D0-9E78-4E17-AA64-C33631A57A8F
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: Close method [App packaging and management], Close method [App packaging and management], IAppxPackageWriter2 interface, Close,IAppxPackageWriter2.Close, IAppxPackageWriter2, IAppxPackageWriter2 interface [App packaging and management], Close method, IAppxPackageWriter2::Close, appxpackaging/IAppxPackageWriter2::Close, appxpkg.iappxpackagewriter2_close
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: AppxPackaging.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxPackageWriter2.Close
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxPackageWriter2::Close method


## -description


Closes the package writer object's output stream.


## -parameters




### -param manifest [in]

The stream that provides the contents of the manifest for the package. The stream must support <a href="https://msdn.microsoft.com/library/windows/hardware/hh439702">Read</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/hh439723">Seek</a>, and <a href="https://msdn.microsoft.com/c22ab396-dbc5-43a0-8448-35a2c094464f">Stat</a>.


### -param contentGroupMap [in]

The stream that provides the contents of the content group map for the package.


## -returns



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
<tr>
<td width="40%">
<dl>
<dt><b>APPX_E_INVALID_MANIFEST</b></dt>
</dl>
</td>
<td width="60%">
The input stream contains a manifest that is not valid. 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/CB3F2FBC-7CCA-45F9-A384-D5458EBA1A7B">IAppxPackageWriter2</a>
 

 

