---
UID: NF:winber.ber_skip_tag
title: ber_skip_tag function
author: windows-sdk-content
description: The ber_skip_tag function skips the current tag and returns the tag of the next element in the supplied BerElement structure.
old-location: ldap\ber_skip_tag.htm
tech.root: ldap
ms.assetid: aa7548db-7752-4ce5-9f24-434abe77b000
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_ldap_ber_skip_tag, ber_skip_tag, ber_skip_tag function [LDAP], ldap.ber__skip__tag, ldap.ber_skip_tag, winber/ber_skip_tag"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wldap32.dll
api_name:
 - ber_skip_tag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ber_skip_tag function


## -description


The <b>ber_skip_tag</b> function skips  the current tag and returns the tag of the next element in the supplied <a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a> structure.


## -parameters




### -param pBerElement [in]

Pointer to the source <a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a> structure.


### -param pLen [out]

Returns the length of the skipped element.


## -returns



Returns the tag of the next element in the <a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a> structure. LBER_DEFAULT is returned if there is no further data to read.




## -remarks



This function is similar to 
<a href="https://msdn.microsoft.com/0c6f24fa-47df-401c-afe8-84bf2987dd36">ber_peek_tag</a>, except that the state pointer, in the 
<a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a> argument, is advanced past the first tag and length, and is pointed to the value part of the next element. This routine should only be used with constructed types and situations when a BER encoding is used as the value of an OCTET STRING.




## -see-also




<a href="https://msdn.microsoft.com/079ac0a6-1b73-433e-88b3-1ce16ddc2851">ber_first_element</a>



<a href="https://msdn.microsoft.com/3daf33c9-730d-4032-a0fc-21de4c425209">ber_next_element</a>



<a href="https://msdn.microsoft.com/0c6f24fa-47df-401c-afe8-84bf2987dd36">ber_peek_tag</a>
 

 

