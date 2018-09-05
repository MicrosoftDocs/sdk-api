---
UID: NS:lpmapi.IS_ADSPEC_BODY
title: IS_ADSPEC_BODY
author: windows-sdk-content
description: The IS_ADSPEC_BODY structure contains Integrated Services Adspec information.
old-location: qos\is_adspec_body.htm
old-project: QOS
ms.assetid: f788e094-0b50-4104-be15-3593f53120c5
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IS_ADSPEC_BODY, IS_ADSPEC_BODY structure [QOS], lpmapi/IS_ADSPEC_BODY, qos.is_adspec_body
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: lpmapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: IS_ADSPEC_BODY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lpmapi.h
api_name:
 - IS_ADSPEC_BODY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IS_ADSPEC_BODY structure


## -description


The 
<b>IS_ADSPEC_BODY</b> structure contains Integrated Services Adspec information.


## -struct-fields




### -field adspec_mh

Main header information and length, expressed as an <a href="https://msdn.microsoft.com/b67fdf53-322b-4a70-ae83-63d4365e9b57">IntServMainHdr</a> structure.


### -field adspec_genparms

General Adspec parameter fragment, followed by variable-length fragments for some or all services.


## -remarks



The variable-length fragments that follow the <b>adspec_genparams</b> member can be minimal length fragments.




## -see-also




<a href="https://msdn.microsoft.com/b67fdf53-322b-4a70-ae83-63d4365e9b57">IntServMainHdr</a>
 

 

