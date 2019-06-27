---
UID: NS:slpublic._tagSL_NONGENUINE_UI_OPTIONS
title: SL_NONGENUINE_UI_OPTIONS (slpublic.h)
author: windows-sdk-content
description: Specifies an application that displays a dialog box when the SLIsGenuineLocal function indicates that an installation is not genuine.
old-location: security\sl_nongenuine_ui_options.htm
tech.root: SecSLApi
ms.assetid: 5e793f09-1d12-4b69-8ba6-6c45421df533
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SL_NONGENUINE_UI_OPTIONS, SL_NONGENUINE_UI_OPTIONS structure [Security], security.sl_nongenuine_ui_options, slpublic/SL_NONGENUINE_UI_OPTIONS
ms.topic: struct
f1_keywords: 
 - "slpublic/SL_NONGENUINE_UI_OPTIONS"
req.header: slpublic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - HeaderDef
api_location:
 - Slpublic.h
api_name:
 - SL_NONGENUINE_UI_OPTIONS
product: Windows
targetos: Windows
req.typenames: SL_NONGENUINE_UI_OPTIONS
req.redist: 
ms.custom: 19H1
---

# SL_NONGENUINE_UI_OPTIONS structure


## -description


Specifies an application that displays a dialog box when the <a href="https://docs.microsoft.com/windows/desktop/api/slpublic/nf-slpublic-slisgenuinelocal">SLIsGenuineLocal</a> function indicates that an installation is not genuine.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field pComponentId

A pointer to an <b>SLID</b> structure that specifies an application that displays a dialog box.


### -field hResultUI

The return value that the <a href="https://docs.microsoft.com/windows/desktop/api/slpublic/nf-slpublic-slisgenuinelocal">SLIsGenuineLocal</a> function returns when an installation is not genuine.

