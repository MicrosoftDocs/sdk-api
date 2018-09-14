---
UID: NN:appxpackaging.IAppxPackageWriter
title: IAppxPackageWriter
author: windows-sdk-content
description: Provides a write-only object model for app packages.
old-location: appxpkg\iappxpackagewriter.htm
tech.root: appxpkg
ms.assetid: 097B7451-9A54-4C39-8F83-16DB49691B42
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IAppxPackageWriter, IAppxPackageWriter interface [App packaging and management], IAppxPackageWriter interface [App packaging and management],described, appxpackaging/IAppxPackageWriter, appxpkg.iappxpackagewriter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IAppxPackageWriter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxPackageWriter interface


## -description


Provides a write-only object model for app packages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxPackageWriter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxPackageWriter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxPackageWriter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2BFC725A-CD56-46CA-983A-FD1BFB6CB474">AddPayloadFile</a>
</td>
<td align="left" width="63%">
Adds a new payload file to the app package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/294625B2-1141-44EE-A769-365C3B37EBD9">Close</a>
</td>
<td align="left" width="63%">
Writes footprint files at the end of the app package, and closes the package writer object's output stream.

</td>
</tr>
</table> 


## -remarks



This object can be retrieved using the <a href="https://msdn.microsoft.com/10E9250E-7A64-4FB0-ACB9-10CB144A0FBE">CreatePackageWriter</a> method of the <a href="https://msdn.microsoft.com/4EA79D44-7C26-4B65-81A1-394E1E540F34">IAppxFactory</a> interface.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/FD677D75-50D5-4228-891F-73B5F40679B0">How to create an app package</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/D34D0909-BE2B-4182-8C3D-36A4E8DDC820">IAppxPackageReader</a>
 

 

