---
UID: NS:winldap.l_timeval
title: LDAP_TIMEVAL (winldap.h)
description: Used to represent an interval of time.
helpviewer_keywords: ["*PLDAP_TIMEVAL","LDAP_TIMEVAL","LDAP_TIMEVAL structure [LDAP]","PLDAP_TIMEVAL","PLDAP_TIMEVAL structure pointer [LDAP]","_ldap_ldap_timeval","ldap.ldap__timeval","ldap.ldap_timeval","winldap/LDAP_TIMEVAL","winldap/PLDAP_TIMEVAL"]
old-location: ldap\ldap_timeval.htm
tech.root: ldap
ms.assetid: 8e551e7c-7237-4761-92e8-c352c3adda77
ms.date: 12/05/2018
ms.keywords: '*PLDAP_TIMEVAL, LDAP_TIMEVAL, LDAP_TIMEVAL structure [LDAP], PLDAP_TIMEVAL, PLDAP_TIMEVAL structure pointer [LDAP], _ldap_ldap_timeval, ldap.ldap__timeval, ldap.ldap_timeval, winldap/LDAP_TIMEVAL, winldap/PLDAP_TIMEVAL'
req.header: winldap.h
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
req.typenames: LDAP_TIMEVAL, *PLDAP_TIMEVAL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - l_timeval
 - winldap/l_timeval
 - PLDAP_TIMEVAL
 - winldap/PLDAP_TIMEVAL
 - LDAP_TIMEVAL
 - winldap/LDAP_TIMEVAL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winldap.h
api_name:
 - LDAP_TIMEVAL
---

# LDAP_TIMEVAL structure


## -description

The <b>LDAP_TIMEVAL</b> structure is used to represent an interval of time.

## -struct-fields

### -field tv_sec

Time interval, in seconds.

### -field tv_usec

Time interval, in microseconds.

## -remarks

The  <b>LDAP_TIMEVAL</b> structure specify both local timeouts and timeouts sent to the server. The exact usage is described in each LDAP function where used.

## -see-also

<a href="/previous-versions/windows/desktop/ldap/data-structures">Data Structures</a>



<a href="/previous-versions/windows/desktop/ldap/searching-a-directory">Searching a Directory</a>