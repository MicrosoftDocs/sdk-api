---
UID: NS:ntdsapi._DS_REPL_KCC_DSA_FAILUREW_BLOB
title: DS_REPL_KCC_DSA_FAILUREW_BLOB (ntdsapi.h)
description: Contains replication state data with respect to a specific inbound replication partner.
helpviewer_keywords: ["DS_REPL_KCC_DSA_FAILUREW_BLOB","DS_REPL_KCC_DSA_FAILUREW_BLOB structure [Active Directory]","ad.ds_repl_kcc_dsa_failurew_blob","msDS-ReplConnectionFailures","msDS-ReplLinkFailures","ntdsapi/DS_REPL_KCC_DSA_FAILUREW_BLOB"]
old-location: ad\ds_repl_kcc_dsa_failurew_blob.htm
tech.root: ad
ms.assetid: b0df588a-2ef1-4870-b304-c6f9e07322b0
ms.date: 12/05/2018
ms.keywords: DS_REPL_KCC_DSA_FAILUREW_BLOB, DS_REPL_KCC_DSA_FAILUREW_BLOB structure [Active Directory], ad.ds_repl_kcc_dsa_failurew_blob, msDS-ReplConnectionFailures, msDS-ReplLinkFailures, ntdsapi/DS_REPL_KCC_DSA_FAILUREW_BLOB
req.header: ntdsapi.h
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DS_REPL_KCC_DSA_FAILUREW_BLOB
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DS_REPL_KCC_DSA_FAILUREW_BLOB
 - ntdsapi/_DS_REPL_KCC_DSA_FAILUREW_BLOB
 - DS_REPL_KCC_DSA_FAILUREW_BLOB
 - ntdsapi/DS_REPL_KCC_DSA_FAILUREW_BLOB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntdsapi.h
api_name:
 - DS_REPL_KCC_DSA_FAILUREW_BLOB
---

# DS_REPL_KCC_DSA_FAILUREW_BLOB structure


## -description

The <b>DS_REPL_KCC_DSA_FAILUREW_BLOB</b> structure contains replication state data with respect to a specific inbound replication partner. This state data is compiled and used by the Knowledge Consistency Checker (KCC) to decide when alternate replication routes must be added to account for  unreachable servers.
  This structure is similar to the <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failurew">DS_REPL_KCC_DSA_FAILURE</a> structure, but is obtained from the <a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">Lightweight Directory Access Protocol API</a> functions when obtaining binary data for the <b>msDS-ReplConnectionFailures</b> or <b>msDS-ReplLinkFailures</b> attribute.

## -struct-fields

### -field oszDsaDN

Contains the offset, in bytes, from the address of this structure  to  a null-terminated string that contains the  distinguished name of the directory system agent object in the directory that corresponds to the source server.

### -field uuidDsaObjGuid

Contains the <b>objectGuid</b> of the directory system agent object represented by the <b>oszDsaDN</b> member.

### -field ftimeFirstFailure

Contains a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure which the contents of depends on the requested binary replication data.



#### msDS-ReplConnectionFailures

Contains the date and time that the first failure occurred when replicating from the source server.



#### msDS-ReplLinkFailures

Contains the date and time of the last successful replication.

### -field cNumFailures

Contains the number of consecutive failures since the last successful replication.

### -field dwLastResult

Contains the error code associated with the most recent failure, or <b>ERROR_SUCCESS</b> if the specific error is unavailable.

## -see-also

<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failurew">DS_REPL_KCC_DSA_FAILURE</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>



<a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">Lightweight Directory Access Protocol API</a>