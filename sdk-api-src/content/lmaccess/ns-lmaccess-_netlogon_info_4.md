---
UID: NS:lmaccess._NETLOGON_INFO_4
title: "_NETLOGON_INFO_4"
author: windows-driver-content
description: Defines a level-4 control query response from a domain controller.
old-location: winprog\netlogon_info_4.htm
old-project: DevNotes
ms.assetid: 6a0ffd68-149f-4d5d-8a8a-69f429ca135a
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: "*PNETLOGON_INFO_4, NETLOGON_INFO_4, NETLOGON_INFO_4 structure [Windows API], PNETLOGON_INFO_4, PNETLOGON_INFO_4 structure pointer [Windows API], _NETLOGON_INFO_4, lmaccess/NETLOGON_INFO_4, lmaccess/PNETLOGON_INFO_4, winprog.netlogon_info_4"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: lmaccess.h
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
req.typenames: NETLOGON_INFO_4, *PNETLOGON_INFO_4
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Lmaccess.h
api_name:
-	NETLOGON_INFO_4
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _NETLOGON_INFO_4 structure


## -description


The <b>NETLOGON_INFO_4</b> structure defines a level-4 control query response from a domain controller.


## -struct-fields




### -field netlog4_trusted_dc_name.string

 


### -field netlog4_trusted_domain_name.string

 


### -field netlog4_trusted_dc_name

A marshaled pointer to a string that contains the trusted domain controller name.


### -field netlog4_trusted_domain_name

A marshaled pointer to a string that contains the trusted domain name.


## -see-also




<a href="https://msdn.microsoft.com/bf40ee60-3a13-4a4e-a0f4-ba7c9fc11097">I_NetLogonControl2</a>
 

 

