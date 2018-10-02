---
UID: NN:fsrm.IFsrmPathMapper
title: IFsrmPathMapper
author: windows-sdk-content
description: Used to retrieve the network share paths that are mapped to a local path.
old-location: fsrm\ifsrmpathmapper.htm
tech.root: Fsrm
ms.assetid: 04e62a10-1719-454b-adfb-6320e31c7a88
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IFsrmPathMapper, IFsrmPathMapper interface [File Server Resource Manager], IFsrmPathMapper interface [File Server Resource Manager],described, fs.ifsrmpathmapper, fsrm.ifsrmpathmapper, fsrm/IFsrmPathMapper
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: fsrm.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h, FsrmTlb.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
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
req.dll: SrmSvc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmPathMapper
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmPathMapper interface


## -description


Used to retrieve the network share paths that are mapped to a local path.

To get this interface, call the 
    <a href="https://msdn.microsoft.com/en-us/library/ms680701(v=VS.85).aspx">CoCreateInstanceEx</a> function. Use 
    <b>CLSID_FsrmPathMapper</b> as the class identifier and 
    <code>__uuidof(IFsrmPathMapper)</code> as the interface identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmPathMapper</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFsrmPathMapper</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFsrmPathMapper</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af5c668f-4675-4568-9b6a-c8d2663d819b">GetSharePathsForLocalPath</a>
</td>
<td align="left" width="63%">
Retrieves a list of network shares that point to the specified local path.

</td>
</tr>
</table> 


## -remarks



To create this object from a script, use the program identifier, "Fsrm.FsrmPathMapper".




## -see-also




<a href="https://msdn.microsoft.com/bbd888d9-1005-4173-8e82-ced13e68c09e">FSRM Interfaces</a>



<a href="https://msdn.microsoft.com/19f7f1d1-7d10-4b73-a158-7c8722958ab5">FsrmPathMapper</a>
 

 

