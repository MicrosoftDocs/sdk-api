---
UID: NF:mssip.CryptSIPRemoveSignedDataMsg
title: CryptSIPRemoveSignedDataMsg function (mssip.h)
author: windows-sdk-content
description: Removes a specified Authenticode signature.
old-location: security\cryptsipremovesigneddatamsg.htm
tech.root: SecCrypto
ms.assetid: c3ea46bb-931a-4ca6-93f5-db7e07b4cb7a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CryptSIPRemoveSignedDataMsg, CryptSIPRemoveSignedDataMsg function [Security], mssip/CryptSIPRemoveSignedDataMsg, security.cryptsipremovesigneddatamsg
ms.topic: function
req.header: mssip.h
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
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptSIPRemoveSignedDataMsg
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CryptSIPRemoveSignedDataMsg function


## -description


The <b>CryptSIPRemoveSignedDataMsg</b> function removes a specified <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">Authenticode</a> signature.


## -parameters




### -param pSubjectInfo [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/mssip/ns-mssip-sip_subjectinfo_">SIP_SUBJECTINFO</a> structure that contains information about the message subject.


### -param dwIndex [in]

This parameter is reserved and should be set to zero.


## -returns



If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns  <b>FALSE</b>. For extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mssip/nf-mssip-cryptsipgetsigneddatamsg">CryptSIPGetSignedDataMsg</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mssip/nf-mssip-cryptsipputsigneddatamsg">CryptSIPPutSignedDataMsg</a>
 

 

