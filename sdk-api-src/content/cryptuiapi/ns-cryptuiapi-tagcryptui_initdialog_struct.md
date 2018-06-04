---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# tagCRYPTUI_INITDIALOG_STRUCT structure


## -description


The <b>CRYPTUI_INITDIALOG_STRUCT</b> structure supports the <a href="https://msdn.microsoft.com/7bbd58df-3a1b-4d82-9a90-7c94260a7165">CRYPTUI_VIEWCERTIFICATE_STRUCT</a> structure. It  is passed as the <i>lParam</i> in the <a href="_win32_wm_initdialog_cpp">WM_INITDIALOG</a> call to each
property sheet that is in the <b>rgPropSheetPages</b> array of the <a href="https://msdn.microsoft.com/7bbd58df-3a1b-4d82-9a90-7c94260a7165">CRYPTUI_VIEWCERTIFICATE_STRUCT</a> structure. The <b>CRYPTUI_VIEWCERTIFICATE_STRUCT</b> structure is used in the <a href="https://msdn.microsoft.com/5107ff22-78c4-4005-80af-ff45781da6c7">CryptUIDlgViewCertificate</a> function.


## -struct-fields




### -field lParam

The <b>lParam</b> in the <a href="_win32_propsheetpage_str_cpp">PROPSHEETPAGE</a> structure.


### -field pCertContext

A pointer to the <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure for the certificate that <a href="https://msdn.microsoft.com/5107ff22-78c4-4005-80af-ff45781da6c7">CryptUIDlgViewCertificate</a> is displaying.


## -see-also




<a href="https://msdn.microsoft.com/7bbd58df-3a1b-4d82-9a90-7c94260a7165">CRYPTUI_VIEWCERTIFICATE_STRUCT</a>



<a href="https://msdn.microsoft.com/5107ff22-78c4-4005-80af-ff45781da6c7">CryptUIDlgViewCertificate</a>
 

 

