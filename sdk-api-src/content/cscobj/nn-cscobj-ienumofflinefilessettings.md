---
UID: NN:cscobj.IEnumOfflineFilesSettings
title: IEnumOfflineFilesSettings (cscobj.h)
author: windows-sdk-content
description: Enumerates setting objects associated with the Offline Files service.
old-location: of\ienumofflinefilessettings.htm
tech.root: offlinefiles
ms.assetid: 2d0e45d5-5559-4c2e-9c20-4e5b84b5fbbd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumOfflineFilesSettings, IEnumOfflineFilesSettings interface [Offline Files], IEnumOfflineFilesSettings interface [Offline Files],described, cscobj/IEnumOfflineFilesSettings, of.ienumofflinefilessettings
ms.topic: interface
f1_keywords: ["cscobj/IEnumOfflineFilesSettings"]
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
 - IEnumOfflineFilesSettings
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumOfflineFilesSettings interface


## -description


Enumerates setting objects associated with the Offline Files service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumOfflineFilesSettings</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumOfflineFilesSettings</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumOfflineFilesSettings</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-ienumofflinefilessettings-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a new instance of the enumerator with the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-ienumofflinefilessettings-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves the next item in the enumeration and advances the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-ienumofflinefilessettings-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-ienumofflinefilessettings-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/offlinefiles/offline-files-api-interfaces">Offline Files API Interfaces</a>
 

 

