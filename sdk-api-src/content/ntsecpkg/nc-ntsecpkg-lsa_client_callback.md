---
UID: NC:ntsecpkg.LSA_CLIENT_CALLBACK
title: LSA_CLIENT_CALLBACK (ntsecpkg.h)
description: Allows a Local Security Authority (LSA)-mode security package to call back to its user-mode package and invoke a function in its DLL there.helpviewer_keywords: ["ClientCallback","ClientCallback callback function [Security]","LSA_CLIENT_CALLBACK","LSA_CLIENT_CALLBACK callback","_ssp_clientcallback","ntsecpkg/ClientCallback","security.clientcallback"]
old-location: security\clientcallback.htm
tech.root: SecAuthN
ms.assetid: d818a7b5-15c8-4d25-a8de-050926f34a9d
ms.date: 12/05/2018
ms.keywords: ClientCallback, ClientCallback callback function [Security], LSA_CLIENT_CALLBACK, LSA_CLIENT_CALLBACK callback, _ssp_clientcallback, ntsecpkg/ClientCallback, security.clientcallback
f1_keywords:
- ntsecpkg/ClientCallback
dev_langs:
- c++
req.header: ntsecpkg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
- UserDefined
api_location:
- Ntsecpkg.h
api_name:
- ClientCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LSA_CLIENT_CALLBACK callback function


## -description


The <b>ClientCallback</b> function allows a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/l-gly">Local Security Authority</a> (LSA)-mode <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security package</a> to call back to its user-mode package and invoke a function in its DLL there.


## -parameters




### -param Callback [in]

A pointer to the name of the function to invoke. For more information, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa374759(v=vs.85)">ClientCallback_Function</a>.


### -param Argument1 [in]

A pointer to the first argument to pass to the callback function.


### -param Argument2 [in]

A pointer to the second argument to pass to the callback function.


### -param Input [in]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/sspi/ns-sspi-secbuffer">SecBuffer</a> structure that contains information to pass to the callback function.


### -param Output [out]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/sspi/ns-sspi-secbuffer">SecBuffer</a> structure that receives information passed from the callback function.


## -returns



If the function succeeds, the function returns STATUS_SUCCESS.

If the function fails, it returns an <b>NTSTATUS</b> code that indicates the reason it failed.




## -remarks



A pointer to the <b>ClientCallback</b> function is available in the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a> function.

The user-mode security package must use the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa379372(v=vs.85)">RegisterCallback</a> function to register the function to be called.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa374759(v=vs.85)">ClientCallback_Function</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa379372(v=vs.85)">RegisterCallback</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spinitializefn">SpInitialize</a>
 

 

