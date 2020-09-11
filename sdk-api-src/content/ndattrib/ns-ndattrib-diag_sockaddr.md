---
UID: NS:ndattrib.tagSOCK_ADDR
title: DIAG_SOCKADDR (ndattrib.h)
description: Stores an Internet Protocol (IP) address for a computer that is participating in a Windows Sockets communication.
helpviewer_keywords: ["*PDIAG_SOCK_ADDR","DIAG_SOCKADDR","DIAG_SOCKADDR structure [NDF]","PDIAG_SOCKADDR","PDIAG_SOCKADDR structure pointer [NDF]","ndattrib/DIAG_SOCKADDR","ndattrib/PDIAG_SOCKADDR","ndf.diag_sockaddr","tagSOCK_ADDR"]
old-location: ndf\diag_sockaddr.htm
tech.root: NDF
ms.assetid: 31da9541-e7d0-4cbc-9d9d-3bcf71acb975
ms.date: 12/05/2018
ms.keywords: '*PDIAG_SOCK_ADDR, DIAG_SOCKADDR, DIAG_SOCKADDR structure [NDF], PDIAG_SOCKADDR, PDIAG_SOCKADDR structure pointer [NDF], ndattrib/DIAG_SOCKADDR, ndattrib/PDIAG_SOCKADDR, ndf.diag_sockaddr, tagSOCK_ADDR'
req.header: ndattrib.h
req.include-header: NDHelper.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: NDHelper.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DIAG_SOCKADDR, *PDIAG_SOCK_ADDR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagSOCK_ADDR
 - ndattrib/tagSOCK_ADDR
 - PDIAG_SOCK_ADDR
 - ndattrib/PDIAG_SOCK_ADDR
 - DIAG_SOCKADDR
 - ndattrib/DIAG_SOCKADDR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ndattrib.h
api_name:
 - DIAG_SOCKADDR
---

# DIAG_SOCKADDR structure


## -description

The <b>DIAG_SOCKADDR</b> structure stores an 
   Internet Protocol (IP) address for a computer that is participating in a Windows Sockets 
   communication.

## -struct-fields

### -field family

Type: <b>USHORT</b>

Socket address group.

### -field data

Type: <b>CHAR[126]</b>

The maximum size of all the different socket address structures.

## -remarks

This data structure is designed to be used as a 
    <b>SOCKADDR</b> structure.

