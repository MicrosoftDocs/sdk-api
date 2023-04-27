---
UID: NE:docobj.OLECMDEXECOPT
title: OLECMDEXECOPT (docobj.h)
description: Specifies command execution options.
helpviewer_keywords: ["OLECMDEXECOPT","OLECMDEXECOPT enumeration [COM]","OLECMDEXECOPT_DODEFAULT","OLECMDEXECOPT_DONTPROMPTUSER","OLECMDEXECOPT_PROMPTUSER","OLECMDEXECOPT_SHOWHELP","_ole_OLECMDEXECOPT","com.olecmdexecopt","docobj/OLECMDEXECOPT","docobj/OLECMDEXECOPT_DODEFAULT","docobj/OLECMDEXECOPT_DONTPROMPTUSER","docobj/OLECMDEXECOPT_PROMPTUSER","docobj/OLECMDEXECOPT_SHOWHELP"]
old-location: com\olecmdexecopt.htm
tech.root: com
ms.assetid: 6245725e-51d4-40e1-8cf1-a65657e790ef
ms.date: 12/05/2018
ms.keywords: OLECMDEXECOPT, OLECMDEXECOPT enumeration [COM], OLECMDEXECOPT_DODEFAULT, OLECMDEXECOPT_DONTPROMPTUSER, OLECMDEXECOPT_PROMPTUSER, OLECMDEXECOPT_SHOWHELP, _ole_OLECMDEXECOPT, com.olecmdexecopt, docobj/OLECMDEXECOPT, docobj/OLECMDEXECOPT_DODEFAULT, docobj/OLECMDEXECOPT_DONTPROMPTUSER, docobj/OLECMDEXECOPT_PROMPTUSER, docobj/OLECMDEXECOPT_SHOWHELP
req.header: docobj.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OLECMDEXECOPT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OLECMDEXECOPT
 - docobj/OLECMDEXECOPT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DocObj.h
api_name:
 - OLECMDEXECOPT
---

# OLECMDEXECOPT enumeration


## -description

Specifies command execution options.

## -enum-fields

### -field OLECMDEXECOPT_DODEFAULT:0

Prompt the user for input or not, whichever is the default behavior.

### -field OLECMDEXECOPT_PROMPTUSER:1

Execute the command after obtaining user input.

### -field OLECMDEXECOPT_DONTPROMPTUSER:2

Execute the command without prompting the user. For example, clicking the Print toolbar button causes a document to be immediately printed without user input.

### -field OLECMDEXECOPT_SHOWHELP:3

Show help for the corresponding command, but do not execute.

## -see-also

<a href="/windows/desktop/api/docobj/nf-docobj-iolecommandtarget-exec">IOleCommandTarget::Exec</a>
