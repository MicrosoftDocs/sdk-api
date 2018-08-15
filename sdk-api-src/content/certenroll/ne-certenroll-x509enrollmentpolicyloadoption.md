---
UID: NE:certenroll.X509EnrollmentPolicyLoadOption
title: X509EnrollmentPolicyLoadOption
author: windows-sdk-content
description: Is used by the LoadPolicy method on the IX509EnrollmentPolicyServer interface to specify how to retrieve policy from the policy server.
old-location: security\x509enrollmentpolicyloadoption.htm
old-project: seccertenroll
ms.assetid: 94adcffd-b4fe-4bd9-912c-9e8d5e5fdb5b
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: LoadOptionCacheOnly, LoadOptionDefault, LoadOptionRegisterForADChanges, LoadOptionReload, X509EnrollmentPolicyLoadOption, X509EnrollmentPolicyLoadOption enumeration [Security], certenroll/LoadOptionCacheOnly, certenroll/LoadOptionDefault, certenroll/LoadOptionRegisterForADChanges, certenroll/LoadOptionReload, certenroll/X509EnrollmentPolicyLoadOption, security.x509enrollmentpolicyloadoption
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: certenroll.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: X509EnrollmentPolicyLoadOption
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Certenroll.h
api_name:
 - X509EnrollmentPolicyLoadOption
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# X509EnrollmentPolicyLoadOption enumeration


## -description


The <b>X509EnrollmentPolicyLoadOption</b> enumeration is used by the <a href="https://msdn.microsoft.com/5b617c6e-91bc-4a22-acd6-41083102850a">LoadPolicy</a> method on the <a href="https://msdn.microsoft.com/e39d40fd-3d43-4cdc-b41a-07a87a11bfad">IX509EnrollmentPolicyServer</a> interface to specify how to retrieve policy from the policy server.


## -enum-fields




### -field LoadOptionDefault

Reload if the cache has expired.


### -field LoadOptionCacheOnly

Always load from the cache even if it has expired.


### -field LoadOptionReload

Always reload.


### -field LoadOptionRegisterForADChanges

Registers a thread to update a sequence number if there are changes to the template or the certification authority container. This value applies only to an Active Directory policy server.


## -see-also




<a href="https://msdn.microsoft.com/5b617c6e-91bc-4a22-acd6-41083102850a">LoadPolicy</a>
 

 

