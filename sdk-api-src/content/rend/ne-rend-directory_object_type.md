---
UID: NE:rend.DIRECTORY_OBJECT_TYPE
title: DIRECTORY_OBJECT_TYPE (rend.h)
description: The DIRECTORY_OBJECT_TYPE enum is a descriptor of whether a directory object is a conference or a user.
helpviewer_keywords: ["DIRECTORY_OBJECT_TYPE","DIRECTORY_OBJECT_TYPE enumeration [TAPI 2.2]","OT_CONFERENCE","OT_USER","_tapi3_directory_object_type","rend/DIRECTORY_OBJECT_TYPE","rend/OT_CONFERENCE","rend/OT_USER","tapi3.directory_object_type"]
old-location: tapi3\directory_object_type.htm
tech.root: tapi3
ms.assetid: 17deac23-a81f-4bb3-a6e5-4105c504c0b5
ms.date: 12/05/2018
ms.keywords: DIRECTORY_OBJECT_TYPE, DIRECTORY_OBJECT_TYPE enumeration [TAPI 2.2], OT_CONFERENCE, OT_USER, _tapi3_directory_object_type, rend/DIRECTORY_OBJECT_TYPE, rend/OT_CONFERENCE, rend/OT_USER, tapi3.directory_object_type
req.header: rend.h
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
targetos: Windows
req.typenames: DIRECTORY_OBJECT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DIRECTORY_OBJECT_TYPE
 - rend/DIRECTORY_OBJECT_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rend.h
api_name:
 - DIRECTORY_OBJECT_TYPE
---

# DIRECTORY_OBJECT_TYPE enumeration


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>DIRECTORY_OBJECT_TYPE</b> enum is a descriptor of whether a directory object is a conference or a user.

## -enum-fields

### -field OT_CONFERENCE:1

Conference.

### -field OT_USER:2

User.

## -see-also

<a href="/windows/desktop/api/rend/nf-rend-itrendezvous-createdirectoryobject">CreateDirectoryObject</a>



<a href="/windows/desktop/api/rend/nf-rend-itdirectory-enumeratedirectoryobjects">EnumerateDirectoryObjects</a>



<a href="/windows/desktop/api/rend/nn-rend-itdirectory">ITDirectory</a>



<a href="/windows/desktop/api/rend/nn-rend-itdirectoryobject">ITDirectoryObject</a>



<a href="/windows/desktop/api/rend/nf-rend-itdirectory-get_directoryobjects">get_DirectoryObjects</a>



<a href="/windows/desktop/api/rend/nf-rend-itdirectoryobject-get_objecttype">get_ObjectType</a>
