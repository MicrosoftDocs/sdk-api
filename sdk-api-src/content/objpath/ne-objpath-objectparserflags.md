---
UID: NE:objpath.ObjectParserFlags
title: ObjectParserFlags (objpath.h)
description: Flags used by constructor for CObjectPathParser.
helpviewer_keywords: ["ObjectParserFlags","ObjectParserFlags enumeration [Windows Management Instrumentation]","e_ParserAbsoluteNamespaceOnly","e_ParserAcceptAll","e_ParserAcceptRelativeNamespace","objpath/ObjectParserFlags","objpath/e_ParserAbsoluteNamespaceOnly","objpath/e_ParserAcceptAll","objpath/e_ParserAcceptRelativeNamespace","wmi.objectparserflags"]
old-location: wmi\objectparserflags.htm
tech.root: wmi
ms.assetid: 25e575fc-c8d3-461c-a792-0780ea56612d
ms.date: 12/05/2018
ms.keywords: ObjectParserFlags, ObjectParserFlags enumeration [Windows Management Instrumentation], e_ParserAbsoluteNamespaceOnly, e_ParserAcceptAll, e_ParserAcceptRelativeNamespace, objpath/ObjectParserFlags, objpath/e_ParserAbsoluteNamespaceOnly, objpath/e_ParserAcceptAll, objpath/e_ParserAcceptRelativeNamespace, wmi.objectparserflags
req.header: objpath.h
req.include-header: Objpath.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
targetos: Windows
req.typenames: ObjectParserFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ObjectParserFlags
 - objpath/ObjectParserFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Objpath.h
api_name:
 - ObjectParserFlags
---

# ObjectParserFlags enumeration


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/objpath/nl-objpath-cobjectpathparser">CObjectPathParser</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

Flags used by constructor for <a href="/windows/desktop/api/objpath/nl-objpath-cobjectpathparser">CObjectPathParser</a>.

## -enum-fields

### -field e_ParserAcceptRelativeNamespace

Allow a relative namespace.

### -field e_ParserAbsoluteNamespaceOnly

Require a full object path.

### -field e_ParserAcceptAll

Accept any recognizable subset of a path.

## -see-also

<a href="/windows/desktop/api/objpath/nl-objpath-cobjectpathparser">CObjectPathParser</a>

