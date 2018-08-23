---
UID: NF:xenroll.ICEnroll4.InstallPKCS7Ex
title: ICEnroll4::InstallPKCS7Ex
author: windows-sdk-content
description: Processes a certificate or chain of certificates, placing them into the appropriate certificate stores.InstallPKCS7 except that it returns the number of certificates actually installed in local stores.
old-location: security\icenroll4_installpkcs7ex.htm
old-project: SecCrypto
ms.assetid: 886fd5f0-d91f-439f-b259-dfb0206d3078
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: CEnroll object [Security],InstallPKCS7Ex method, ICEnroll4 interface [Security],InstallPKCS7Ex method, ICEnroll4.InstallPKCS7Ex, ICEnroll4::InstallPKCS7Ex, InstallPKCS7Ex, InstallPKCS7Ex method [Security], InstallPKCS7Ex method [Security],CEnroll object, InstallPKCS7Ex method [Security],ICEnroll4 interface, _xen_icenroll4_installpkcs7ex, security.icenroll4_installpkcs7ex, xenroll/ICEnroll4::InstallPKCS7Ex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xenroll.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: XBL_IDP_AUTH_TOKEN_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - ICEnroll4.InstallPKCS7Ex
 - CEnroll.InstallPKCS7Ex
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# ICEnroll4::InstallPKCS7Ex


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>InstallPKCS7Ex</b> method processes a certificate or chain of certificates, placing them into the appropriate <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate stores</a>. The <b>InstallPKCS7Ex</b> method is the same as 
<a href="https://msdn.microsoft.com/63482360-0d8a-4e23-8942-8276630778a3">InstallPKCS7</a> except that it returns the number of certificates actually installed in local stores. This method was first defined in the <a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a> interface.


## -parameters




### -param PKCS7 [in]

A string that contains a certificate or chain of certificates.


### -param plCertInstalled [out]

Returns the number of certificates installed into local stores.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 A <b>Long</b> that contains the number of certificates installed into local stores.




## -remarks



When this method is called from script, the method displays a user interface that asks whether the user will allow installation of a  certificate.




## -see-also




<a href="https://msdn.microsoft.com/7f13549d-811b-496b-abdd-7e52cbc2ed54">CEnroll</a>



<a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a>



<a href="https://msdn.microsoft.com/63482360-0d8a-4e23-8942-8276630778a3">InstallPKCS7</a>



<a href="https://msdn.microsoft.com/5a428d83-c846-4f44-a682-58c3e025c353">acceptPKCS7</a>
 

 

