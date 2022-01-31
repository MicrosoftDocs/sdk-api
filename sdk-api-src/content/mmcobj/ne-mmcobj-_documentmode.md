---
UID: NE:mmcobj.DocumentMode
title: _DocumentMode (mmcobj.h)
description: The DocumentMode enumeration is used by the Document.Mode property and specifies how the document is opened. This enumeration applies to the MMC 2.0 Automation Object Model.
helpviewer_keywords: ["*PDOCUMENTMODE","DOCUMENTMODE","DocumentMode","DocumentMode enumeration [MMC]","DocumentMode_Author","DocumentMode_User","DocumentMode_User_MDI","DocumentMode_User_SDI","PDOCUMENTMODE","PDOCUMENTMODE enumeration pointer [MMC]","PPDOCUMENTMODE","PPDOCUMENTMODE enumeration pointer [MMC]","_DocumentMode","_DocumentMode enumeration [MMC]","_slate_documentmode","mmc.documentmode","mmcobj/DocumentMode","mmcobj/DocumentMode_Author","mmcobj/DocumentMode_User","mmcobj/DocumentMode_User_MDI","mmcobj/DocumentMode_User_SDI","mmcobj/PDOCUMENTMODE","mmcobj/PPDOCUMENTMODE"]
old-location: mmc\documentmode.htm
tech.root: mmc
ms.assetid: 62a215e1-a993-4994-a1b1-86a8c320758d
ms.date: 12/05/2018
ms.keywords: '*PDOCUMENTMODE, DOCUMENTMODE, DocumentMode, DocumentMode enumeration [MMC], DocumentMode_Author, DocumentMode_User, DocumentMode_User_MDI, DocumentMode_User_SDI, PDOCUMENTMODE, PDOCUMENTMODE enumeration pointer [MMC], PPDOCUMENTMODE, PPDOCUMENTMODE enumeration pointer [MMC], _DocumentMode, _DocumentMode enumeration [MMC], _slate_documentmode, mmc.documentmode, mmcobj/DocumentMode, mmcobj/DocumentMode_Author, mmcobj/DocumentMode_User, mmcobj/DocumentMode_User_MDI, mmcobj/DocumentMode_User_SDI, mmcobj/PDOCUMENTMODE, mmcobj/PPDOCUMENTMODE'
req.header: mmcobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MmcObj.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: _DocumentMode, DOCUMENTMODE, *PDOCUMENTMODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DocumentMode
 - mmcobj/DocumentMode
 - PDOCUMENTMODE
 - mmcobj/PDOCUMENTMODE
 - _DocumentMode
 - mmcobj/_DocumentMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - MmcObj.h
api_name:
 - _DocumentMode
---

# _DocumentMode enumeration


## -description

The 
<b>DocumentMode</b> enumeration is used by the 
<a href="/previous-versions/windows/desktop/mmc/document-mode">Document.Mode</a> property and specifies how the document is opened. This enumeration applies to the 
<a href="/previous-versions/windows/desktop/mmc/mmc-2-0-automation-object-model">MMC 2.0 Automation Object Model</a>.

## -enum-fields

### -field DocumentMode_Author:0

The document is opened in Author Mode.

### -field DocumentMode_User

The document is opened in Full-Access User Mode.

### -field DocumentMode_User_MDI

The document is opened in Limited-Access User Mode with multiple windows.

### -field DocumentMode_User_SDI

The document is opened in Limited-Access User Mode with a single window.

## -see-also

<a href="/previous-versions/windows/desktop/mmc/document-object">Document object</a>



<a href="/previous-versions/windows/desktop/mmc/document-mode">Document.Mode</a>
