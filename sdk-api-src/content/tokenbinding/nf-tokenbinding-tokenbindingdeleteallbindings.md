---
UID: NF:tokenbinding.TokenBindingDeleteAllBindings
title: TokenBindingDeleteAllBindings function
author: windows-sdk-content
description: Deletes all token binding keys that are associated with the calling user or app container.
old-location: security\tokenbindingdeleteallbindings.htm
tech.root: seccng
ms.assetid: 0446F62F-96B4-4F4B-9789-0CD12173E601
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TokenBindingDeleteAllBindings, TokenBindingDeleteAllBindings function [Security], security.tokenbindingdeleteallbindings, tokenbinding/TokenBindingDeleteAllBindings
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: tokenbinding.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Tokenbinding.lib
req.dll: Tokenbinding.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - tokenbinding.dll
api_name:
 - TokenBindingDeleteAllBindings
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TokenBindingDeleteAllBindings function


## -description


Deletes all token binding keys that are associated with the calling user or app container.


## -parameters






## -returns



Returns a status code that indicates the success or failure of the function. 




## -remarks



You can call <b>TokenBindingDeleteAllBindings</b> from user mode. 




## -see-also




<a href="https://msdn.microsoft.com/4258CC92-580E-403C-9AE4-4BB726255464">TokenBindingDeleteBinding</a>



<a href="https://msdn.microsoft.com/4289E3F0-17AC-485B-A326-2C8BECD5CABB">TokenBindingGenerateBinding</a>
 

 

