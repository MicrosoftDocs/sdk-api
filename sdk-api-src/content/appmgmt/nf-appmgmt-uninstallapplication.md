---
UID: NF:appmgmt.UninstallApplication
title: UninstallApplication function (appmgmt.h)
description: The UninstallApplication function uninstalls a group policy application that handles setup and installation using Windows Installer .msi files.
helpviewer_keywords: ["UninstallApplication","UninstallApplication function [Group Policy]","appmgmt/UninstallApplication","policy.uninstallapplication"]
old-location: policy\uninstallapplication.htm
tech.root: Policy
ms.assetid: d45494e2-d86e-4d94-a158-4024eacf46a2
ms.date: 12/05/2018
ms.keywords: UninstallApplication, UninstallApplication function [Group Policy], appmgmt/UninstallApplication, policy.uninstallapplication
req.header: appmgmt.h
req.include-header: 
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UninstallApplication
 - appmgmt/UninstallApplication
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - UninstallApplication
---

# UninstallApplication function


## -description

The
    <b>UninstallApplication</b> function uninstalls a group policy  application that handles setup and installation using <a href="/windows/desktop/Msi/windows-installer-portal">Windows Installer</a> .msi files. The <b>UninstallApplication</b> function should only be called in the context of the user for whom the user group policy application has previously attempted an uninstall by calling the <a href="/windows/desktop/api/msi/nf-msi-msiconfigureproducta">MsiConfigureProduct</a> function. The <a href="/windows/desktop/api/appmgmt/nf-appmgmt-installapplication">InstallApplication</a> function can install group policy applications.
<div class="alert"><b>Note</b>  Failure to call <b>UninstallApplication</b> as part of the protocol for uninstalling a group policy-based application can cause the <a href="/previous-versions/windows/desktop/Policy/reporting-group-policy">Resultant Set of Policy (RSoP)</a> to indicate inaccurate information.</div><div> </div>

## -parameters

### -param ProductCode [in]

The <a href="/windows/desktop/Msi/windows-installer-portal">Windows Installer</a> product code of the product being uninstalled. The <a href="/windows/desktop/Msi/product-codes">product code</a> of the application should be provided in the form of  a <a href="/windows/desktop/Msi/guid">Windows Installer GUID</a> as a string with braces.

### -param dwStatus [in]

The status of the uninstall attempt. The <i>dwStatus</i> parameter is the Windows success code of the uninstall attempt returned by <a href="/windows/desktop/api/msi/nf-msi-msiconfigureproducta">MsiConfigureProduct</a>.  The system can use this to ensure that the  <a href="/previous-versions/windows/desktop/Policy/reporting-group-policy">Resultant Set of Policy (RSoP)</a> indicates whether the uninstall failed or succeeded.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>. Otherwise, the function returns one of the system error codes. For a complete list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a> or the header file WinError.h.

## -remarks

Remove a group policy application that uses .msi files by calling  the <a href="/windows/desktop/Msi/windows-installer-portal">Windows Installer</a> function <a href="/windows/desktop/api/msi/nf-msi-msiconfigureproducta">MsiConfigureProduct</a> to uninstall the application. Then call <b>UninstallApplication</b>  to  inform the system that the application is no longer managed on the client by Group Policy.  <b>UninstallApplication</b> should be called even if the uninstall fails because this enables the system to keep the <a href="/previous-versions/windows/desktop/Policy/reporting-group-policy">Resultant Set of Policy (RSoP)</a> accurate.

Remove applications installed using software installation settings (.zap files) by calling  the uninstall function or command  specific for the installation application. For information about using installation applications other than  the <a href="/windows/desktop/Msi/windows-installer-portal">Windows Installer</a> see article 231747, "How to Publish non-MSI Programs with .zap Files," in the Microsoft Knowledge Base.

## -see-also

<a href="/previous-versions/windows/desktop/Policy/group-policy-functions">Group Policy
    Functions</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/windows/desktop/api/appmgmt/nf-appmgmt-installapplication">InstallApplication</a>



<a href="/windows/desktop/api/msi/nf-msi-msiconfigureproducta">MsiConfigureProduct</a>