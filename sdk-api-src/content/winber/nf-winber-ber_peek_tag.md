---
UID: NF:winber.ber_peek_tag
title: ber_peek_tag function
author: windows-sdk-content
description: Returns the tag of the next element to be parsed in the supplied BerElement structure.
old-location: ldap\ber_peek_tag.htm
old-project: LDAP
ms.assetid: 0c6f24fa-47df-401c-afe8-84bf2987dd36
ms.author: windowssdkdev
ms.date: 05/15/2018
ms.keywords: "_ldap_ber_peek_tag, ber_peek_tag, ber_peek_tag function [LDAP], ldap.ber__peek__tag, ldap.ber_peek_tag, winber/ber_peek_tag"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winber.h
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
req.typenames: WIN32_STREAM_ID, *LPWIN32_STREAM_ID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wldap32.dll
api_name:
-	ber_peek_tag
product: Windows
targetos: Windows
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ber_peek_tag function


## -description


The <b>ber_peek_tag</b> function returns the tag of the next element to be parsed in the supplied <a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a> structure.


## -parameters




### -param pBerElement [in]

Pointer to the source <a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a> structure.


### -param pLen [out]

Returns the length of the next element to be parsed.


## -returns



Returns the tag of the next element to be read in the <a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a> structure. LBER_DEFAULT is returned if there is no further data to be read.




## -remarks



The decoding position within the <i>pBerElement</i> parameter is unchanged by this call; that is, the fact that <b>ber_peek_tag</b> has been called does not affect future use of the <a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/079ac0a6-1b73-433e-88b3-1ce16ddc2851">ber_first_element</a>



<a href="https://msdn.microsoft.com/3daf33c9-730d-4032-a0fc-21de4c425209">ber_next_element</a>



<a href="https://msdn.microsoft.com/aa7548db-7752-4ce5-9f24-434abe77b000">ber_skip_tag</a>
 

 

