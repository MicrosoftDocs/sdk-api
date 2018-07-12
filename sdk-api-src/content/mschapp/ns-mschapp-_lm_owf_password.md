---
UID: NS:mschapp._LM_OWF_PASSWORD
title: "_LM_OWF_PASSWORD"
author: windows-sdk-content
description: The LM_OWF_PASSWORD stores the Lan Manage (LM) one-way function (OWF) of a user's password.
old-location: mschap\lm_owf_password.htm
old-project: mschap
ms.assetid: db155f34-fa57-4449-9319-d46561fd18c0
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: "*PLM_OWF_PASSWORD, *PNT_OWF_PASSWORD, LM_OWF_PASSWORD, LM_OWF_PASSWORD structure [MS-CHAP], NT_OWF_PASSWORD, PLM_OWF_PASSWORD, PLM_OWF_PASSWORD structure pointer [MS-CHAP], _LM_OWF_PASSWORD, mschap.lm_owf_password, mschapp/LM_OWF_PASSWORD, mschapp/PLM_OWF_PASSWORD"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: LM_OWF_PASSWORD
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - MsChapp.h
api_name:
 - LM_OWF_PASSWORD
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _LM_OWF_PASSWORD structure


## -description


The <b>LM_OWF_PASSWORD</b> stores the Lan Manage (LM) one-way function (OWF) of a user's password.


## -struct-fields




### -field data

An array of <a href="https://msdn.microsoft.com/eb0e38ed-8d12-4df2-be58-7ac18447121f">CYPHER_BLOCK</a> structures that contain a LM OWF password hash. The contents of the array are calculated using the <b>LmEncryptedPasswordHash()</b> function as defined in <a href="http://go.microsoft.com/fwlink/p/?linkid=84041">RFC 2433</a>, section A.8.


## -remarks




<a href="https://msdn.microsoft.com/7edba7de-e3b8-4a93-b70b-19c68541da1e">NT_OWF_PASSWORD</a> is an alias for this structure.




## -see-also




<a href="https://msdn.microsoft.com/adee58bd-d2aa-4570-8c43-50240be02ed3">MS-CHAP Password Management Structures</a>



<a href="https://msdn.microsoft.com/6c154675-4c82-4305-8231-577f990eaeb1">MSChapSrvChangePassword</a>
 

 

