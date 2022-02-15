---
UID: NS:ctfutb.TF_LANGBARITEMINFO
title: TF_LANGBARITEMINFO (ctfutb.h)
description: The TF_LANGBARITEMINFO structure is used to hold information about a language bar item.
helpviewer_keywords: ["TF_LANGBARITEMINFO","TF_LANGBARITEMINFO structure [Text Services Framework]","_tsf_tf_langbariteminfo_ref","ctfutb/TF_LANGBARITEMINFO","tsf.tf_langbariteminfo"]
old-location: tsf\tf_langbariteminfo.htm
tech.root: TSF
ms.assetid: 4a826a2c-4cae-4cbf-8a25-38337dcd498d
ms.date: 12/05/2018
ms.keywords: TF_LANGBARITEMINFO, TF_LANGBARITEMINFO structure [Text Services Framework], _tsf_tf_langbariteminfo_ref, ctfutb/TF_LANGBARITEMINFO, tsf.tf_langbariteminfo
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
targetos: Windows
req.typenames: TF_LANGBARITEMINFO
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - TF_LANGBARITEMINFO
 - ctfutb/TF_LANGBARITEMINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ctfutb.h
api_name:
 - TF_LANGBARITEMINFO
---

# TF_LANGBARITEMINFO structure


## -description

The <b>TF_LANGBARITEMINFO</b> structure is used to hold information about a language bar item.

## -struct-fields

### -field clsidService

Contains the <b>CLSID</b> of the text service that owns the language bar item. This can be CLSID_NULL if the item is not provided by a text service.

### -field guidItem

Contains a <b>GUID</b> value that identifies the language bar item.

Starting with Windows 8, this value should be GUID_LBI_INPUTMODE (or the language bar item will be ignored). For more information, see [Third-party input method editors](https://docs.microsoft.com/en-us/windows/win32/w8cookbook/third-party-input-method-editors#manifestation) in the Compatibility cookbook for Windows.

### -field dwStyle

Contains a combination of one or more of the <a href="/windows/desktop/TSF/tf-lbi-style--constants">TF_LBI_STYLE_*</a> values.

### -field ulSort

Specifies the sort order of the language bar item, relative to other language bar items owned by the text service. A lower number indicates that the item will be displayed prior to an item with a higher sort number.

This value is only used if <b>clsidService</b> identifies a registered text service. For more information about registering a text service, see <a href="/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-register">ITfInputProcessorProfiles::Register</a>.

### -field szDescription

Contains the description string for the item in Unicode format. The description string is displayed in the language bar options menu for menu items. This buffer can hold up to TF_LBI_DESC_MAXLEN characters.

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-register">ITfInputProcessorProfiles::Register
      </a>



<a href="/windows/desktop/TSF/tf-lbi-style--constants">TF_LBI_STYLE_*
      </a>
