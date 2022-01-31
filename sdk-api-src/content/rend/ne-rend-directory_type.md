---
UID: NE:rend.DIRECTORY_TYPE
title: DIRECTORY_TYPE (rend.h)
description: The DIRECTORY_TYPE enum is used to indicate the type of directory server.
helpviewer_keywords: ["DIRECTORY_TYPE","DIRECTORY_TYPE enumeration [TAPI 2.2]","DT_ILS","DT_NTDS","_tapi3_directory_type","rend/DIRECTORY_TYPE","rend/DT_ILS","rend/DT_NTDS","tapi3.directory_type"]
old-location: tapi3\directory_type.htm
tech.root: tapi3
ms.assetid: dd4292f0-ca76-4464-b0fb-288ce5813a40
ms.date: 12/05/2018
ms.keywords: DIRECTORY_TYPE, DIRECTORY_TYPE enumeration [TAPI 2.2], DT_ILS, DT_NTDS, _tapi3_directory_type, rend/DIRECTORY_TYPE, rend/DT_ILS, rend/DT_NTDS, tapi3.directory_type
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
req.typenames: DIRECTORY_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DIRECTORY_TYPE
 - rend/DIRECTORY_TYPE
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
 - DIRECTORY_TYPE
---

# DIRECTORY_TYPE enumeration


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>DIRECTORY_TYPE</b> enum is used to indicate the type of directory server.

## -enum-fields

### -field DT_NTDS:1

Directory type is NTDS.

### -field DT_ILS:2

Directory type is ILS. The ILS directory type is valid only for Windows 2000 and not for Windows XP.

## -see-also

<a href="/windows/desktop/api/rend/nf-rend-itrendezvous-createdirectory">CreateDirectory</a>



<a href="/windows/desktop/api/rend/nn-rend-itdirectory">ITDirectory</a>



<a href="/windows/desktop/api/rend/nn-rend-itrendezvous">ITRendezvous</a>



<a href="/windows/desktop/api/rend/nf-rend-itdirectory-get_directorytype">get_DirectoryType</a>
