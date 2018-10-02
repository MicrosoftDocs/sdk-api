---
UID: NS:ctfutb.TF_LANGBARITEMINFO
title: TF_LANGBARITEMINFO
author: windows-sdk-content
description: The TF_LANGBARITEMINFO structure is used to hold information about a language bar item.
old-location: tsf\tf_langbariteminfo.htm
tech.root: TSF
ms.assetid: 4a826a2c-4cae-4cbf-8a25-38337dcd498d
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: TF_LANGBARITEMINFO, TF_LANGBARITEMINFO structure [Text Services Framework], _tsf_tf_langbariteminfo_ref, ctfutb/TF_LANGBARITEMINFO, tsf.tf_langbariteminfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ctfutb.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctfutb.idl
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
 - Ctfutb.h
api_name:
 - TF_LANGBARITEMINFO
product: Windows
targetos: Windows
req.typenames: TF_LANGBARITEMINFO
req.redist: TSF 1.0 on Windows 2000 Professional
---

# TF_LANGBARITEMINFO structure


## -description



The <b>TF_LANGBARITEMINFO</b> structure is used to hold information about a language bar item.




## -struct-fields




### -field clsidService

Contains the <b>CLSID</b> of the text service that owns the language bar item. This can be CLSID_NULL if the item is not provided by a text service.


### -field guidItem

Contains a <b>GUID</b> value that identifies the language bar item.


### -field dwStyle

Contains a combination of one or more of the <a href="https://msdn.microsoft.com/9180a666-774f-401b-bea3-68d5396fab30">TF_LBI_STYLE_*</a> values.


### -field ulSort

Specifies the sort order of the language bar item, relative to other language bar items owned by the text service. A lower number indicates that the item will be displayed prior to an item with a higher sort number.

This value is only used if <b>clsidService</b> identifies a registered text service. For more information about registering a text service, see <a href="https://msdn.microsoft.com/264bc32e-60a2-4dff-a212-5682d30a769e">ITfInputProcessorProfiles::Register</a>.


### -field szDescription

Contains the description string for the item in Unicode format. The description string is displayed in the language bar options menu for menu items. This buffer can hold up to TF_LBI_DESC_MAXLEN characters.


## -see-also




<a href="https://msdn.microsoft.com/264bc32e-60a2-4dff-a212-5682d30a769e">ITfInputProcessorProfiles::Register
      </a>



<a href="https://msdn.microsoft.com/9180a666-774f-401b-bea3-68d5396fab30">TF_LBI_STYLE_*
      </a>
 

 

