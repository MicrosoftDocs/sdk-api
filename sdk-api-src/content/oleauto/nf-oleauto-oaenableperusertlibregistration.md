---
UID: NF:oleauto.OaEnablePerUserTLibRegistration
title: OaEnablePerUserTLibRegistration function (oleauto.h)
description: Enables the RegisterTypeLib function to override default registry mappings under Windows Vista Service Pack 1 (SP1), Windows Server 2008, and later operating system versions.
helpviewer_keywords: ["OaEnablePerUserTLibRegistration","OaEnablePerUserTLibRegistration function [Automation]","_oa96_OaEnablePerUserTlibRegistration","automat.oaenableperusertlibregistration","oleauto/OaEnablePerUserTLibRegistration"]
old-location: automat\oaenableperusertlibregistration.htm
tech.root: automat
ms.assetid: 356af9a9-77f9-4699-abc3-ab3ff1db2915
ms.date: 12/05/2018
ms.keywords: OaEnablePerUserTLibRegistration, OaEnablePerUserTLibRegistration function [Automation], _oa96_OaEnablePerUserTlibRegistration, automat.oaenableperusertlibregistration, oleauto/OaEnablePerUserTLibRegistration
req.header: oleauto.h
req.include-header: 
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
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OaEnablePerUserTLibRegistration
 - oleauto/OaEnablePerUserTLibRegistration
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - OaEnablePerUserTLibRegistration
---

# OaEnablePerUserTLibRegistration function


## -description

Enables the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-registertypelib">RegisterTypeLib</a> function to override default registry mappings under Windows Vista Service Pack 1 (SP1), Windows Server 2008, and later operating system versions.



## -remarks

Consider the following scenario: You are running an application on a computer that is running Windows Vista SP1 or later. In your application, you have overridden the HKEY_CLASSES_ROOT registry subtree and mapped it to another registry subtree. (For example, perhaps you mapped HKEY_CLASSES_ROOT to HKEY_CURRENT_USER.) You then attempt to register a type library by calling <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-registertypelib">RegisterTypeLib</a>, and you receive an "access denied" error message. Additionally, <b>RegisterTypeLib</b> returns the TYPE_E_REGISTRYACCESS (0x8002801c) value.



This problem occurs if User Account Control (UAC) is enabled, and the application is running under a limited user account.



You can resolve this problem in one of two ways:



<ul>
<li>
Use the <b>OaEnablePerUserTLibRegistration</b> function. Before your application calls <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-registertypelib">RegisterTypeLib</a>, it should call <b>OaEnablePerUserTLibRegistration</b>. This enables <b>RegisterTypeLib</b> to accept the registry override mapping. The <b>OaEnablePerUserTLibRegistration</b> function is exported from the Oleaut32.dll file. You must reference this file by using run-time dynamic linking and the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> function.



</li>
<li>
Set the OAPERUSERTLIBREG environment variable. <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-registertypelib">RegisterTypeLib</a> will check the value of this variable. If the value of OAPERUSERTLIBREG is 1, <b>RegisterTypeLib</b> will use the appropriate override mapping. Because this environment variable is read during the initialization of the <b>DLLMain</b> function, you must set the variable before you run your application. To do this, run one of the following commands at a command prompt:



<b>set OAPERUSERTLIBREG=1</b>

- or -



<b>start cmd.exe /c "set OAPERUSERTLIBREG=1 &amp;&amp; </b><i>MyApp.exe</i><b>"

</b>

</li>
</ul>
When using run-time dynamic linking it should be noted that the setting to enable per-user type library registration is a global setting in oleaut32.dll, so if oleaut32.dll is unloaded then this setting is lost.
