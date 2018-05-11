---
UID: NE:wtypes.tagSTATFLAG
title: tagSTATFLAG
author: windows-driver-content
description: Indicate whether the method should try to return a name in the pwcsName member of the STATSTG structure.
old-location: stg\statflag.htm
old-project: Stg
ms.assetid: 9070b517-8ca5-455f-baee-0647b1895c08
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: STATFLAG, STATFLAG enumeration [Structured Storage], STATFLAG_DEFAULT, STATFLAG_NONAME, STATFLAG_NOOPEN, _stg_statflag, stg.statflag, tagSTATFLAG, wtypes/STATFLAG, wtypes/STATFLAG_DEFAULT, wtypes/STATFLAG_NONAME, wtypes/STATFLAG_NOOPEN
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: STATFLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WTypes.h
api_name:
-	STATFLAG
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagSTATFLAG enumeration


## -description



			The 
<b>STATFLAG</b> enumeration values indicate whether the method should try to return a name in the <b>pwcsName</b> member of the 
<a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a> structure. The values are used in the 
<a href="https://msdn.microsoft.com/e7953f21-ac34-44e3-9b6f-b93ac89e2e32">ILockBytes::Stat</a>, 
<a href="https://msdn.microsoft.com/87478fa8-1b5f-44ed-bffc-e139c7f44a12">IStorage::Stat</a>, and 
<a href="https://msdn.microsoft.com/c22ab396-dbc5-43a0-8448-35a2c094464f">IStream::Stat</a> methods to save memory when the <b>pwcsName</b> member is not required.


## -enum-fields




### -field STATFLAG_DEFAULT

Requests that the statistics include the <b>pwcsName</b> member of the 
<a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a> structure.


### -field STATFLAG_NONAME

Requests that the statistics not include the <b>pwcsName</b> member of the 
<a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a> structure. If the name is omitted, there is no need for the 
<a href="https://msdn.microsoft.com/e7953f21-ac34-44e3-9b6f-b93ac89e2e32">ILockBytes::Stat</a>, 
<a href="https://msdn.microsoft.com/87478fa8-1b5f-44ed-bffc-e139c7f44a12">IStorage::Stat</a>, and 
<a href="https://msdn.microsoft.com/c22ab396-dbc5-43a0-8448-35a2c094464f">IStream::Stat</a> methods methods to allocate and free memory for the string value of the name, therefore the method reduces time and resources used in an allocation and free operation.


### -field STATFLAG_NOOPEN

Not implemented.


## -see-also




<a href="https://msdn.microsoft.com/e7953f21-ac34-44e3-9b6f-b93ac89e2e32">ILockBytes::Stat</a>



<a href="https://msdn.microsoft.com/87478fa8-1b5f-44ed-bffc-e139c7f44a12">IStorage::Stat</a>



<a href="https://msdn.microsoft.com/c22ab396-dbc5-43a0-8448-35a2c094464f">IStream::Stat</a>
 

 

