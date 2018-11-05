---
UID: NS:winldap.l_timeval
title: l_timeval
author: windows-sdk-content
description: Used to represent an interval of time.
old-location: ldap\ldap_timeval.htm
tech.root: ldap
ms.assetid: 8e551e7c-7237-4761-92e8-c352c3adda77
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*PLDAP_TIMEVAL, LDAP_TIMEVAL, LDAP_TIMEVAL structure [LDAP], PLDAP_TIMEVAL, PLDAP_TIMEVAL structure pointer [LDAP], _ldap_ldap_timeval, l_timeval, ldap.ldap__timeval, ldap.ldap_timeval, winldap/LDAP_TIMEVAL, winldap/PLDAP_TIMEVAL"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winldap.h
api_name:
 - LDAP_TIMEVAL
product: Windows
targetos: Windows
req.typenames: LDAP_TIMEVAL, *PLDAP_TIMEVAL
req.redist: 
---

# l_timeval structure


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




<a href="https://msdn.microsoft.com/1af7ea80-a65b-42bf-a1b2-ca54c173c9fb">Data Structures</a>



<a href="https://msdn.microsoft.com/38482501-faa1-4055-9758-e1e0a4199688">Searching a Directory</a>
 

 

