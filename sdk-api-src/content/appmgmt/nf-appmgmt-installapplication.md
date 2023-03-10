---
UID: NF:appmgmt.InstallApplication
title: InstallApplication function (appmgmt.h)
description: The InstallApplication function can install applications that have been deployed to target users that belong to a domain.
helpviewer_keywords: ["InstallApplication","InstallApplication function [Group Policy]","appmgmt/InstallApplication","policy.installapplication"]
old-location: policy\installapplication.htm
tech.root: Policy
ms.assetid: 5b2e1d82-a421-42af-9e1b-391ae9d4813e
ms.date: 12/05/2018
ms.keywords: InstallApplication, InstallApplication function [Group Policy], appmgmt/InstallApplication, policy.installapplication
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
 - InstallApplication
 - appmgmt/InstallApplication
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - ext-ms-win-advapi32-msi-l1-1-0.dll
api_name:
 - InstallApplication
req.apiset: ext-ms-win-advapi32-msi-l1-1-0 (introduced in Windows 8)
---

# InstallApplication function


## -description

The <b>InstallApplication</b> function can install applications  that have been deployed to target users that belong to a domain. The security context of the user that is calling <b>InstallApplication</b> must be that of a domain user logged onto a computer in a domain that trusts the target user's domain. Group Policy must be successfully applied when the target user logs on.

## -parameters

### -param pInstallInfo [in]

A pointer to a <a href="/windows/desktop/api/appmgmt/ns-appmgmt-installdata">INSTALLDATA</a> structure that specifies the application to install.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>. Otherwise, the function returns one of the system error codes. For a complete list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a> or the header file WinError.h.

## -remarks

The <b>InstallApplication</b> function can only install applications that have been deployed by using  Group Policy. A domain administrator can deploy applications to  target users by using  the  user configuration section of Group Policy Objects (GPO). The target user must belong to the target domain and the GPO must apply to this  user in the target  domain. The <b>InstallApplication</b> function installs applications according to standard Group Policy inheritance rules.  If the same application is deployed in multiple GPOs, the function installs the version of the application deployed in the highest precedence GPO.  After an application has been  installed for a user, it is not visible to other users on the computer. This is standard for applications that are deployed through user group policy.

The <b>InstallApplication</b> function can  install deployed applications that  use <a href="/windows/desktop/Msi/windows-installer-portal">Windows Installer</a> (.msi files) or software installation settings (.zap files) to handle setup and installation.

The
    <b>InstallApplication</b> function can install applications that use a <a href="/windows/desktop/Msi/windows-installer-portal">Windows Installer</a> package for their installation.  In this case,  the  user calling <b>InstallApplication</b> is not required to have administrator privileges. The system can install the application because the  Windows Installer  is a trusted application deployed by a domain administrator. The user that receives the application must have access to the location of the .msi files.

Remove applications installed using .msi files by calling the <a href="/windows/desktop/Msi/windows-installer-portal">Windows Installer</a> function <a href="/windows/desktop/api/msi/nf-msi-msiconfigureproducta">MsiConfigureProduct</a> to uninstall the application. Then call <a href="/windows/desktop/api/appmgmt/nf-appmgmt-uninstallapplication">UninstallApplication</a>  to  inform the system that the application is no longer managed on the client by Group Policy.  <b>UninstallApplication</b> should be called even if the uninstall fails because this enables the system to keep the <a href="/previous-versions/windows/desktop/Policy/reporting-group-policy">Resultant Set of Policy (RSoP)</a> accurate.

The
    <b>InstallApplication</b> function can also install applications that use setup applications based on software installation settings (.zap files). The user that receives the application must have access to the location of the .zap files. A .zap file is a text file similar to an .ini file, which enables Windows to publish an application (for example, Setup.exe) for installation with <b>Add or Remove Programs</b>. To publish applications that do not use the <a href="/windows/desktop/Msi/windows-installer-portal">Windows Installer</a>, you must create a .zap file, copy the .zap file to the software distribution point servers, and then use Group Policy–based software deployment to publish the application for users. 
If the application is deployed using .zap files, the user installing the application must have privileges on the machine to install the software. You cannot use .zap files for assigned applications.

Remove applications using software installation settings (.zap files) by calling the uninstall function or a command  specific for the installation application.

For information about using installation applications other than  the <a href="/windows/desktop/Msi/windows-installer-portal">Windows Installer</a> see article 231747, "How to Publish non-MSI Programs with .zap Files," in the Microsoft Knowledge Base.

## -see-also

<a href="/previous-versions/windows/desktop/Policy/group-policy-functions">Group Policy
    Functions</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/windows/desktop/api/appmgmt/ns-appmgmt-installdata">INSTALLDATA</a>



<a href="/windows/desktop/api/msi/nf-msi-msiconfigureproducta">MsiConfigureProduct</a>



<a href="/previous-versions/windows/desktop/Policy/reporting-group-policy">Reporting Group Policy</a>



<a href="/windows/desktop/api/appmgmt/nf-appmgmt-uninstallapplication">UninstallApplication</a>



<a href="/windows/desktop/Msi/windows-installer-portal">Windows Installer</a>
