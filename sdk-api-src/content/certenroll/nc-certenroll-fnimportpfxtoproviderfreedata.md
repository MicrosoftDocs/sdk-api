---
UID: NC:certenroll.FNIMPORTPFXTOPROVIDERFREEDATA
title: FNIMPORTPFXTOPROVIDERFREEDATA
author: windows-sdk-content
description: Frees PFX certificate context(s).
old-location: security\fnimportpfxtoproviderfreedata.htm
tech.root: seccrypto
ms.assetid: F3A28405-8D6E-4930-946B-FB7D9B6518B9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "(FNIMPORTPFXTOPROVIDERFREEDATA), (FNIMPORTPFXTOPROVIDERFREEDATA) callback function [Security], FNIMPORTPFXTOPROVIDERFREEDATA callback, certenroll/(FNIMPORTPFXTOPROVIDERFREEDATA), fnimportpfxtoproviderfreedata, security.fnimportpfxtoproviderfreedata, wincrypt/(FNIMPORTPFXTOPROVIDERFREEDATA)"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: certenroll.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - certenroll.h
 - wincrypt.h
api_name:
 - (FNIMPORTPFXTOPROVIDERFREEDATA)
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FNIMPORTPFXTOPROVIDERFREEDATA callback function


## -description


Frees PFX certificate context(s).


## -parameters




### -param cCert [in]

DWORD of the number of certificate contexts to free.


### -param *rgpCert [in, optional]

Pointer to a certificate Context containing to free.

