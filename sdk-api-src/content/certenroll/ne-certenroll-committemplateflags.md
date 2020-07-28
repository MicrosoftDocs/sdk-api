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
f1_keywords:
- certenroll/CommitTemplateFlags
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Certenroll.h
api_name:
- CommitTemplateFlags
targetos: Windows
req.typenames: CommitTemplateFlags
req.redist: 
ms.custom: 19H1
---

# CommitTemplateFlags enumeration


## -description


The <b>CommitTemplateFlags</b> enumeration type specifies options for saving and deleting templates. It is used by the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificatetemplatewritable-commit">Commit</a> method on the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509certificatetemplatewritable">IX509CertificateTemplateWritable</a> interface.


## -enum-fields




### -field CommitFlagSaveTemplateGenerateOID

Save the template and create an object identifier for it.


### -field CommitFlagSaveTemplateUseCurrentOID

Not used.


### -field CommitFlagSaveTemplateOverwrite

Not used.


### -field CommitFlagDeleteTemplate

Delete the template.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificatetemplatewritable-commit">Commit</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509certificatetemplatewritable">IX509CertificateTemplateWritable</a>
 

 

