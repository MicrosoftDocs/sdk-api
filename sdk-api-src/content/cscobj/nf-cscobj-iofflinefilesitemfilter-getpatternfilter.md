---
UID: NF:cscobj.IOfflineFilesItemFilter.GetPatternFilter
title: IOfflineFilesItemFilter::GetPatternFilter
author: windows-driver-content
description: Provides a filter pattern string to limit enumerated items based on item name patterns.
old-location: of\iofflinefilesitemfilter_getpatternfilter.htm
old-project: OfflineFiles
ms.assetid: 570cf25c-d4a4-42d6-8f33-bb660a7e99ab
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetPatternFilter, GetPatternFilter method [Offline Files], GetPatternFilter method [Offline Files],IOfflineFilesItemFilter interface, IOfflineFilesItemFilter interface [Offline Files],GetPatternFilter method, IOfflineFilesItemFilter.GetPatternFilter, IOfflineFilesItemFilter::GetPatternFilter, cscobj/IOfflineFilesItemFilter::GetPatternFilter, of.iofflinefilesitemfilter_getpatternfilter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: OFFLINEFILES_SYNC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CscSvc.dll
-	CscObj.dll
api_name:
-	IOfflineFilesItemFilter.GetPatternFilter
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesItemFilter::GetPatternFilter


## -description



    Provides a filter pattern string to limit enumerated items based on item name patterns. Note that pattern filtering is available only for inclusion filters.  If you provide a pattern filter as an exclusion filter, it is ignored.


## -parameters




### -param pszPattern [out]

Receives the filter pattern string. Pattern strings can contain the * and ? wildcard characters.

Examples:

<ul>
<li>*.DOC</li>
<li>ABC.*</li>
<li>AB?.??2</li>
</ul>

### -param cchPattern [in]

Specifies the maximum length in characters of the buffer receiving the pattern string.  This value is currently <b>MAX_PATH</b>.


## -returns



Returns <b>S_OK</b> if the filter supports pattern filtering and the filter string is successfully copied to the pszPattern buffer.

Returns <b>E_NOTIMPL</b> if pattern filtering is not supported.

Any other error value causes the creation of the enumerator to fail.




## -remarks



While this method can be implemented in any filter type (inclusion, exclusion) or filter target (file, container), it is called only for inclusion filters and file targets.  This method will never be called for any other filter type/target combination.




## -see-also




<a href="https://msdn.microsoft.com/e77b4f90-7a08-47f8-b297-8c1360167e1f">IOfflineFilesItemFilter</a>
 

 

