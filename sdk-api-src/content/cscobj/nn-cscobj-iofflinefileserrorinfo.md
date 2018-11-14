---
UID: NN:cscobj.IOfflineFilesErrorInfo
title: IOfflineFilesErrorInfo
author: windows-sdk-content
description: Provides a text description and raw data block associated with an error.
old-location: of\iofflinefileserrorinfo.htm
tech.root: OfflineFiles
ms.assetid: 6c78d475-aa63-49e4-863f-1a197801f2f9
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IOfflineFilesErrorInfo, IOfflineFilesErrorInfo interface [Offline Files], IOfflineFilesErrorInfo interface [Offline Files],described, cscobj/IOfflineFilesErrorInfo, of.iofflinefileserrorinfo
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
 - IOfflineFilesErrorInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesErrorInfo interface


## -description


Provides a text description and raw data block associated with an error.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesErrorInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IOfflineFilesErrorInfo</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesErrorInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530518(v=VS.85).aspx">GetDescription</a>
</td>
<td align="left" width="63%">
Retrieves a text string describing the error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530519(v=VS.85).aspx">GetRawData</a>
</td>
<td align="left" width="63%">
Retrieves a block of bytes containing internal data associated with the error.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530659(v=VS.85).aspx">Offline Files API Interfaces</a>
 

 

