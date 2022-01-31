---
UID: NE:certenroll.X509EnrollmentPolicyExportFlags
title: X509EnrollmentPolicyExportFlags (certenroll.h)
description: Is used by the Export method on the IX509EnrollmentPolicyServer interface to specify what items to export from the policy server.
helpviewer_keywords: ["ExportCAs","ExportOIDs","ExportTemplates","X509EnrollmentPolicyExportFlags","X509EnrollmentPolicyExportFlags enumeration [Security]","certenroll/ExportCAs","certenroll/ExportOIDs","certenroll/ExportTemplates","certenroll/X509EnrollmentPolicyExportFlags","security.x509enrollmentpolicyexportflags"]
old-location: security\x509enrollmentpolicyexportflags.htm
tech.root: security
ms.assetid: 219f58af-66e8-4a89-8908-89308fc182d8
ms.date: 12/05/2018
ms.keywords: ExportCAs, ExportOIDs, ExportTemplates, X509EnrollmentPolicyExportFlags, X509EnrollmentPolicyExportFlags enumeration [Security], certenroll/ExportCAs, certenroll/ExportOIDs, certenroll/ExportTemplates, certenroll/X509EnrollmentPolicyExportFlags, security.x509enrollmentpolicyexportflags
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
req.typenames: X509EnrollmentPolicyExportFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - X509EnrollmentPolicyExportFlags
 - certenroll/X509EnrollmentPolicyExportFlags
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
 - X509EnrollmentPolicyExportFlags
---

# X509EnrollmentPolicyExportFlags enumeration


## -description

The <b>X509EnrollmentPolicyExportFlags</b> enumeration is used by the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-export">Export</a> method on the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentpolicyserver">IX509EnrollmentPolicyServer</a> interface to specify what items to export from the policy server.

## -enum-fields

### -field ExportTemplates:0x1

Export templates.

### -field ExportOIDs:0x2

Export custom object identifiers.

### -field ExportCAs:0x4

Not used.

## -remarks

To export both templates and object identifiers, specify a bitwise <b>OR</b> of the <b>ExportTemplates</b> and <b>ExportOIDs</b> values.

## -see-also

<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-export">Export</a>
