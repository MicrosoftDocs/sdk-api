---
UID: NF:xenroll.ICEnroll3.InstallPKCS7
title: ICEnroll3::InstallPKCS7
author: windows-sdk-content
description: Processes a certificate or chain of certificates, placing them into the appropriate certificate stores. This method differs from the acceptPKCS7 method in that InstallPKCS7 does not receive a request certificate.
old-location: security\icenroll4_installpkcs7.htm
old-project: SecCrypto
ms.assetid: 63482360-0d8a-4e23-8942-8276630778a3
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CEnroll object [Security],InstallPKCS7 method, ICEnroll3 interface [Security],InstallPKCS7 method, ICEnroll3.InstallPKCS7, ICEnroll3::InstallPKCS7, ICEnroll4 interface [Security],InstallPKCS7 method, ICEnroll4::InstallPKCS7, InstallPKCS7, InstallPKCS7 method [Security], InstallPKCS7 method [Security],CEnroll object, InstallPKCS7 method [Security],ICEnroll3 interface, InstallPKCS7 method [Security],ICEnroll4 interface, security.icenroll4_installpkcs7, xenroll/ICEnroll3::InstallPKCS7, xenroll/ICEnroll4::InstallPKCS7
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xenroll.h
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
 - ICEnroll4.InstallPKCS7
 - ICEnroll3.InstallPKCS7
 - CEnroll.InstallPKCS7
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# ICEnroll3::InstallPKCS7


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>InstallPKCS7</b> method processes a certificate or chain of certificates, placing them into the appropriate <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate stores</a>. This method differs from the  <a href="https://msdn.microsoft.com/5a428d83-c846-4f44-a682-58c3e025c353">acceptPKCS7</a> method in that  <b>InstallPKCS7</b> does not receive a request certificate. This method was first defined in the <a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a> interface.


## -parameters




### -param PKCS7 [in]

A string that contains a certificate or chain of certificates.


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



When this method is called from script, the method displays a user interface that asks whether the user will allow installation of a  certificate.




## -see-also




<a href="https://msdn.microsoft.com/7f13549d-811b-496b-abdd-7e52cbc2ed54">CEnroll</a>



<a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>



<a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a>



<a href="https://msdn.microsoft.com/5a428d83-c846-4f44-a682-58c3e025c353">ICEnroll::acceptPKCS7</a>
 

 

