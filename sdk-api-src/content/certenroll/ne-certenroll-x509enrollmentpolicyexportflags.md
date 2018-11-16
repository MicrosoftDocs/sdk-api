---
UID: NE:certenroll.X509EnrollmentPolicyExportFlags
title: X509EnrollmentPolicyExportFlags
author: windows-sdk-content
description: Is used by the Export method on the IX509EnrollmentPolicyServer interface to specify what items to export from the policy server.
old-location: security\x509enrollmentpolicyexportflags.htm
tech.root: SecCertEnroll
ms.assetid: 219f58af-66e8-4a89-8908-89308fc182d8
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ExportCAs, ExportOIDs, ExportTemplates, X509EnrollmentPolicyExportFlags, X509EnrollmentPolicyExportFlags enumeration [Security], certenroll/ExportCAs, certenroll/ExportOIDs, certenroll/ExportTemplates, certenroll/X509EnrollmentPolicyExportFlags, security.x509enrollmentpolicyexportflags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
 - X509EnrollmentPolicyExportFlags
product: Windows
targetos: Windows
req.typenames: X509EnrollmentPolicyExportFlags
req.redist: 
---

# X509EnrollmentPolicyExportFlags enumeration


## -description


The <b>X509EnrollmentPolicyExportFlags</b> enumeration is used by the <a href="https://msdn.microsoft.com/en-us/library/Ee351694(v=VS.85).aspx">Export</a> method on the <a href="https://msdn.microsoft.com/en-us/library/Ee351692(v=VS.85).aspx">IX509EnrollmentPolicyServer</a> interface to specify what items to export from the policy server.


## -enum-fields




### -field ExportTemplates

Export templates.


### -field ExportOIDs

Export custom object identifiers.


### -field ExportCAs

Not used.


## -remarks



To export both templates and object identifiers, specify a bitwise <b>OR</b> of the <b>ExportTemplates</b> and <b>ExportOIDs</b> values.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ee351694(v=VS.85).aspx">Export</a>
 

 

