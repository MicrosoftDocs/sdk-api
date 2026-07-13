---
UID: NE:certenroll.CommitTemplateFlags
title: CommitTemplateFlags (certenroll.h)
description: Specifies options for saving and deleting templates.
helpviewer_keywords: ["CommitFlagDeleteTemplate","CommitFlagSaveTemplateGenerateOID","CommitFlagSaveTemplateOverwrite","CommitFlagSaveTemplateUseCurrentOID","CommitTemplateFlags","CommitTemplateFlags enumeration [Security]","certenroll/CommitFlagDeleteTemplate","certenroll/CommitFlagSaveTemplateGenerateOID","certenroll/CommitFlagSaveTemplateOverwrite","certenroll/CommitFlagSaveTemplateUseCurrentOID","certenroll/CommitTemplateFlags","security.committemplateflags"]
old-location: security\committemplateflags.htm
tech.root: security
ms.assetid: e228928a-ef11-4caa-b33f-fe25a3a6ff86
ms.date: 12/05/2018
ms.keywords: CommitFlagDeleteTemplate, CommitFlagSaveTemplateGenerateOID, CommitFlagSaveTemplateOverwrite, CommitFlagSaveTemplateUseCurrentOID, CommitTemplateFlags, CommitTemplateFlags enumeration [Security], certenroll/CommitFlagDeleteTemplate, certenroll/CommitFlagSaveTemplateGenerateOID, certenroll/CommitFlagSaveTemplateOverwrite, certenroll/CommitFlagSaveTemplateUseCurrentOID, certenroll/CommitTemplateFlags, security.committemplateflags
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: CommitTemplateFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CommitTemplateFlags
 - certenroll/CommitTemplateFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Certenroll.h
api_name:
 - CommitTemplateFlags
---

# CommitTemplateFlags enumeration


## -description

The <b>CommitTemplateFlags</b> enumeration type specifies options for saving and deleting templates. It is used by the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificatetemplatewritable-commit">Commit</a> method on the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificatetemplatewritable">IX509CertificateTemplateWritable</a> interface.

## -enum-fields

### -field CommitFlagSaveTemplateGenerateOID:1

Save the template and create an object identifier for it.

### -field CommitFlagSaveTemplateUseCurrentOID:2

Not used.

### -field CommitFlagSaveTemplateOverwrite:3

Not used.

### -field CommitFlagDeleteTemplate:4

Delete the template.

## -see-also

<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificatetemplatewritable-commit">Commit</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificatetemplatewritable">IX509CertificateTemplateWritable</a>
