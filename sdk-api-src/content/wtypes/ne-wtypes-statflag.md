---
UID: NE:wtypes.tagSTATFLAG
title: STATFLAG (wtypes.h)
author: windows-sdk-content
description: Indicate whether the method should try to return a name in the pwcsName member of the STATSTG structure.
old-location: stg\statflag.htm
tech.root: Stg
ms.assetid: 9070b517-8ca5-455f-baee-0647b1895c08
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: STATFLAG, STATFLAG enumeration [Structured Storage], STATFLAG_DEFAULT, STATFLAG_NONAME, STATFLAG_NOOPEN, _stg_statflag, stg.statflag, wtypes/STATFLAG, wtypes/STATFLAG_DEFAULT, wtypes/STATFLAG_NONAME, wtypes/STATFLAG_NOOPEN
ms.topic: enum
req.header: wtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WTypes.idl
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
 - WTypes.h
api_name:
 - STATFLAG
product: Windows
targetos: Windows
req.typenames: STATFLAG
req.redist: 
ms.custom: 19H1
---

# STATFLAG enumeration


## -description


The 
<b>STATFLAG</b> enumeration values indicate whether the method should try to return a name in the <b>pwcsName</b> member of the 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-tagstatstg">STATSTG</a> structure. The values are used in the 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ilockbytes-stat">ILockBytes::Stat</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-stat">IStorage::Stat</a>, and 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istream-stat">IStream::Stat</a> methods to save memory when the <b>pwcsName</b> member is not required.


## -enum-fields




### -field STATFLAG_DEFAULT

Requests that the statistics include the <b>pwcsName</b> member of the 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-tagstatstg">STATSTG</a> structure.


### -field STATFLAG_NONAME

Requests that the statistics not include the <b>pwcsName</b> member of the 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-tagstatstg">STATSTG</a> structure. If the name is omitted, there is no need for the 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ilockbytes-stat">ILockBytes::Stat</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-stat">IStorage::Stat</a>, and 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istream-stat">IStream::Stat</a> methods methods to allocate and free memory for the string value of the name, therefore the method reduces time and resources used in an allocation and free operation.


### -field STATFLAG_NOOPEN

Not implemented.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ilockbytes-stat">ILockBytes::Stat</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-stat">IStorage::Stat</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istream-stat">IStream::Stat</a>
 

 

