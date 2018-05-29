---
UID: NS:mscat.CATALOG_INFO_
title: CATALOG_INFO_
author: windows-sdk-content
description: The CATALOG_INFO structure contains the name of a catalog file. This structure is used by the CryptCATCatalogInfoFromContext function.
old-location: security\catalog_info.htm
old-project: SecCrypto
ms.assetid: f6e66412-3ed2-48d9-a377-5df11500db59
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: CATALOG_INFO, CATALOG_INFO structure [Security], CATALOG_INFO_, mscat/CATALOG_INFO, security.catalog_info
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mscat.h
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
req.typenames: CATALOG_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mscat.h
api_name:
-	CATALOG_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# CATALOG_INFO_ structure


## -description


<p class="CCE_Message">[The  <b>CATALOG_INFO</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CATALOG_INFO</b> structure contains the name of a catalog file. This structure is used by the <a href="https://msdn.microsoft.com/ec195fcc-1cff-4dd6-9075-c4904b653da7">CryptCATCatalogInfoFromContext</a> function.


## -struct-fields




### -field cbStruct

Specifies the size, in bytes, of this structure.


### -field wszCatalogFile

Name of the catalog file.


## -see-also




<a href="https://msdn.microsoft.com/ec195fcc-1cff-4dd6-9075-c4904b653da7">CryptCATCatalogInfoFromContext</a>
 

 

