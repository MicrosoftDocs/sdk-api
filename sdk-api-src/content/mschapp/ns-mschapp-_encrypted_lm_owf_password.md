---
UID: NS:mschapp._ENCRYPTED_LM_OWF_PASSWORD
title: "_ENCRYPTED_LM_OWF_PASSWORD"
author: windows-driver-content
description: The ENCRYPTED_LM_OWF_PASSWORD stores a user's encrypted Lan Manager (LM) one-way function (OWF) password hash.
old-location: mschap\encrypted_lm_owf_password.htm
old-project: MsChap
ms.assetid: 83498d3f-0ac5-435c-804e-a4baa1ae855d
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: "*PENCRYPTED_LM_OWF_PASSWORD, *PENCRYPTED_NT_OWF_PASSWORD, ENCRYPTED_LM_OWF_PASSWORD, ENCRYPTED_LM_OWF_PASSWORD structure [MS-CHAP], ENCRYPTED_NT_OWF_PASSWORD, _ENCRYPTED_LM_OWF_PASSWORD, mschap.encrypted_lm_owf_password, mschapp/ENCRYPTED_LM_OWF_PASSWORD"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mschapp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ENCRYPTED_LM_OWF_PASSWORD, *PENCRYPTED_LM_OWF_PASSWORD
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	MsChapp.h
api_name:
-	ENCRYPTED_LM_OWF_PASSWORD
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _ENCRYPTED_LM_OWF_PASSWORD structure


## -description


The <b>ENCRYPTED_LM_OWF_PASSWORD</b> stores a user's encrypted Lan Manager (LM) one-way function (OWF) password hash.


## -struct-fields




### -field data

An array of <a href="https://msdn.microsoft.com/eb0e38ed-8d12-4df2-be58-7ac18447121f">CYPHER_BLOCK</a> structures that contain an encrypted LM OWF password hash. The contents of the array are calculated using the <b>OldLmPasswordHashEncryptedWithNewNtPasswordHash()</b> function as defined in <a href="http://go.microsoft.com/fwlink/p/?linkid=84041">RFC 2433</a>, section A.16.


## -see-also




<a href="https://msdn.microsoft.com/adee58bd-d2aa-4570-8c43-50240be02ed3">MS-CHAP Password Management Structures</a>



<a href="https://msdn.microsoft.com/91ea4b98-79e4-4764-a580-a622d1491943">MSChapSrvChangePassword2</a>
 

 

