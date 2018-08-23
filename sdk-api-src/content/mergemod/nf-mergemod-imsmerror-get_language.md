---
UID: NF:mergemod.IMsmError.get_Language
title: IMsmError::get_Language
author: windows-sdk-content
description: The read-only Language property of the Error object returns the LANGID of the current error.
old-location: setup\error_language.htm
old-project: msi
ms.assetid: f47cad5d-8e76-4210-b1ab-377d2d05379e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Error object,Language property, Error.Language, IMsmError.get_Language, IMsmError::get_Language, Language property, Language property,Error object, _msi_language_property_error_object_, get_Language, setup.error_language
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mergemod.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 1.0 or later
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
tech.root: 
req.typenames: WIN32_MEMORY_REGION_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mergemod.dll
api_name:
 - Error.Language
 - IMsmError.get_Language
product: Windows
targetos: Windows
req.lib: 
req.dll: Mergemod.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMsmError::get_Language


## -description


The read-only 
<b>Language</b> property of the 
<a href="https://msdn.microsoft.com/38025e21-2d31-40f8-a088-2d3912c2893e">Error</a> object returns the <b>LANGID</b> of the current error.

This property is read-only.


## -parameters


## -remarks



The value of the 
<b>Language</b> property is -1 unless the error is of type msmErrorLanguageUnsupported or msmErrorLanguageFailed. You can determine the type of error by calling the 
<a href="https://msdn.microsoft.com/5567ba71-c815-4434-962c-aa46cd171712">Type</a> property of the 
<a href="https://msdn.microsoft.com/38025e21-2d31-40f8-a088-2d3912c2893e">Error</a> object.

<h3><a id="C__"></a><a id="c__"></a>C++</h3>
See 
<a href="https://msdn.microsoft.com/c0d14c18-facc-441c-89c6-85abe6d19443">get_Language Function (Error Object)</a>.



