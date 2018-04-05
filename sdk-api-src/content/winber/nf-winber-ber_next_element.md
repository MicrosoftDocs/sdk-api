---
UID: NF:winber.ber_next_element
title: ber_next_element function
author: windows-driver-content
description: The ber_next_element function is used along with ber_first_element to traverse a SET, SET OF, SEQUENCE or SEQUENCE OF data value stored in the supplied BerElement structure. It returns the tag and length of the next element in the constructed type.
old-location: ldap\ber_next_element.htm
old-project: LDAP
ms.assetid: 3daf33c9-730d-4032-a0fc-21de4c425209
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: "_ldap_ber_next_element, ber_next_element, ber_next_element function [LDAP], ldap.ber__next__element, ldap.ber_next_element, winber/ber_next_element"
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
req.typenames: WIN32_STREAM_ID, *LPWIN32_STREAM_ID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wldap32.dll
api_name:
-	ber_next_element
product: Windows
targetos: Windows
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ber_next_element function


## -description


The <b>ber_next_element</b> function is used along with 
<a href="https://msdn.microsoft.com/079ac0a6-1b73-433e-88b3-1ce16ddc2851">ber_first_element</a> to traverse a SET, SET OF, SEQUENCE or SEQUENCE OF data value stored in the supplied <a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a> structure. It returns the tag and length of the next element in the constructed type.


## -parameters




### -param pBerElement [in]

Pointer to the source <a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a> structure.


### -param pLen [in, out]

Returns the length of the next element to be parsed.


### -param opaque [in, out]

An opaque cookie used internally that was returned by the initial call to the 
<a href="https://msdn.microsoft.com/079ac0a6-1b73-433e-88b3-1ce16ddc2851">ber_first_element</a> function.


## -returns



Returns the tag of the next element to be read in the <a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a> structure. LBER_DEFAULT is returned if there is no further data to be read.




## -remarks



The <i>pLen</i> and <i>opaque</i> pointer values returned by the function are internal parsing state values, and should not be used by applications other than as arguments to subsequent calls of this function.




## -see-also




<a href="https://msdn.microsoft.com/079ac0a6-1b73-433e-88b3-1ce16ddc2851">ber_first_element</a>



<a href="https://msdn.microsoft.com/0c6f24fa-47df-401c-afe8-84bf2987dd36">ber_peek_tag</a>



<a href="https://msdn.microsoft.com/aa7548db-7752-4ce5-9f24-434abe77b000">ber_skip_tag</a>
 

 

