---
UID: NS:ndattrib.tagSOCK_ADDR
title: tagSOCK_ADDR
author: windows-sdk-content
description: Stores an Internet Protocol (IP) address for a computer that is participating in a Windows Sockets communication.
old-location: ndf\diag_sockaddr.htm
old-project: ndf
ms.assetid: 31da9541-e7d0-4cbc-9d9d-3bcf71acb975
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*PDIAG_SOCK_ADDR, DIAG_SOCKADDR, DIAG_SOCKADDR structure [NDF], PDIAG_SOCKADDR, PDIAG_SOCKADDR structure pointer [NDF], ndattrib/DIAG_SOCKADDR, ndattrib/PDIAG_SOCKADDR, ndf.diag_sockaddr, tagSOCK_ADDR"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: DIAG_SOCKADDR, *PDIAG_SOCK_ADDR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ndattrib.h
api_name:
 - DIAG_SOCKADDR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# tagSOCK_ADDR structure


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



