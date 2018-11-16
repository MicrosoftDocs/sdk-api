---
UID: NN:cscobj.IOfflineFilesFileSysInfo
title: IOfflineFilesFileSysInfo
author: windows-sdk-content
description: Represents the standard information associated with a file system item in the Offline Files cache.
old-location: of\iofflinefilesfilesysinfo.htm
tech.root: OfflineFiles
ms.assetid: d3da183d-eb12-4411-b461-b58689ef5bff
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IOfflineFilesFileSysInfo, IOfflineFilesFileSysInfo interface [Offline Files], IOfflineFilesFileSysInfo interface [Offline Files],described, cscobj/IOfflineFilesFileSysInfo, of.iofflinefilesfilesysinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
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
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesFileSysInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesFileSysInfo interface


## -description


Represents the standard information associated with a file system item in the Offline Files cache.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesFileSysInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IOfflineFilesFileSysInfo</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesFileSysInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530569(v=VS.85).aspx">GetAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the Win32 attributes for an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530570(v=VS.85).aspx">GetFileSize</a>
</td>
<td align="left" width="63%">
Retrieves the size of an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530571(v=VS.85).aspx">GetTimes</a>
</td>
<td align="left" width="63%">
Retrieves the time values associated with an item.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530659(v=VS.85).aspx">Offline Files API Interfaces</a>
 

 

