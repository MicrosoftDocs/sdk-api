---
UID: NS:tapi.lineproviderentry_tag
title: LINEPROVIDERENTRY (tapi.h)
author: windows-sdk-content
description: The LINEPROVIDERENTRY structure provides the information for a single service provider entry. An array of these structures is returned as part of the LINEPROVIDERLIST structure returned by the function lineGetProviderList.
old-location: tapi2\lineproviderentry_str.htm
tech.root: Tapi
ms.assetid: e54a8244-e773-441f-a387-b3b22c4a0a54
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPLINEPROVIDERENTRY, LINEPROVIDERENTRY, LINEPROVIDERENTRY structure [TAPI 2.2], LPLINEPROVIDERENTRY, LPLINEPROVIDERENTRY structure pointer [TAPI 2.2], _tapi2_lineproviderentry_str, tapi/LINEPROVIDERENTRY, tapi/LPLINEPROVIDERENTRY, tapi2.lineproviderentry_str"
ms.topic: struct
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINEPROVIDERENTRY
product: Windows
targetos: Windows
req.typenames: LINEPROVIDERENTRY, *LPLINEPROVIDERENTRY
req.redist: 
ms.custom: 19H1
---

# LINEPROVIDERENTRY structure


## -description


The 
<b>LINEPROVIDERENTRY</b> structure provides the information for a single service provider entry. An array of these structures is returned as part of the 
<a href="https://msdn.microsoft.com/75790ffd-bb1b-4efc-a905-5727d31f8aec">LINEPROVIDERLIST</a> structure returned by the function 
<a href="https://msdn.microsoft.com/87d43409-e8c5-401a-87a2-02568ed0af4a">lineGetProviderList</a>.


## -struct-fields




### -field dwPermanentProviderID

Permanent provider identifier of the entry.


### -field dwProviderFilenameSize

Size of the provider file name string, including the <b>null</b> terminator, in bytes.


### -field dwProviderFilenameOffset

Offset from the beginning of the 
<a href="https://msdn.microsoft.com/75790ffd-bb1b-4efc-a905-5727d31f8aec">LINEPROVIDERLIST</a> structure to a <b>null</b>-terminated string containing the file name (path) of the service provider DLL (.TSP) file. The size of the string is specified by <b>dwProviderFilenameSize</b>.


## -remarks



Not extensible.




## -see-also




<a href="https://msdn.microsoft.com/75790ffd-bb1b-4efc-a905-5727d31f8aec">LINEPROVIDERLIST</a>



<a href="https://msdn.microsoft.com/87d43409-e8c5-401a-87a2-02568ed0af4a">lineGetProviderList</a>
 

 

