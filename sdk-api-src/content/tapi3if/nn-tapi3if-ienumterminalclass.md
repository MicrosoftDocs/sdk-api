---
UID: NN:tapi3if.IEnumTerminalClass
title: IEnumTerminalClass (tapi3if.h)
description: The IEnumTerminalClass interface provides COM-standard enumeration methods to discover and use the dynamic terminal classes that are available. The ITTerminalSupport::EnumerateDynamicTerminalClasses method returns a pointer to this interface.
helpviewer_keywords: ["IEnumTerminalClass","IEnumTerminalClass interface [TAPI 2.2]","IEnumTerminalClass interface [TAPI 2.2]","described","_tapi3_ienumterminalclass","tapi3.ienumterminalclass","tapi3if/IEnumTerminalClass"]
old-location: tapi3\ienumterminalclass.htm
tech.root: tapi3
ms.assetid: 1da0a82a-fde4-440c-ac6c-e9b85a7ec3fe
ms.date: 12/05/2018
ms.keywords: IEnumTerminalClass, IEnumTerminalClass interface [TAPI 2.2], IEnumTerminalClass interface [TAPI 2.2],described, _tapi3_ienumterminalclass, tapi3.ienumterminalclass, tapi3if/IEnumTerminalClass
req.header: tapi3if.h
req.include-header: Tapi3.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumTerminalClass
 - tapi3if/IEnumTerminalClass
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - IEnumTerminalClass
---

# IEnumTerminalClass interface


## -description

The 
<b>IEnumTerminalClass</b> interface provides COM-standard enumeration methods to discover and use the dynamic terminal classes that are available. The 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses">ITTerminalSupport::EnumerateDynamicTerminalClasses</a> method returns a pointer to this interface.

The 
<b>IEnumTerminalClass</b> interface is hidden from Visual Basic and scripting languages.

## -inheritance

The <b>IEnumTerminalClass</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumTerminalClass</b> also has these types of members:

## -see-also

<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a>
