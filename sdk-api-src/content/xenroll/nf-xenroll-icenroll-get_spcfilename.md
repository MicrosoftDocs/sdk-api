---
UID: NF:xenroll.ICEnroll.get_SPCFileName
title: ICEnroll::get_SPCFileName (xenroll.h)
description: Sets or retrieves the name of the file to which to write the base64-encoded PKCS (Get)
helpviewer_keywords: ["CEnroll object [Security]","SPCFileName property","ICEnroll interface [Security]","SPCFileName property","ICEnroll.SPCFileName","ICEnroll.get_SPCFileName","ICEnroll2 interface [Security]","SPCFileName property","ICEnroll2.SPCFileName","ICEnroll2::get_SPCFileName","ICEnroll2::put_SPCFileName","ICEnroll3 interface [Security]","SPCFileName property","ICEnroll3.SPCFileName","ICEnroll3::get_SPCFileName","ICEnroll3::put_SPCFileName","ICEnroll4 interface [Security]","SPCFileName property","ICEnroll4.SPCFileName","ICEnroll4::SPCFileName","ICEnroll4::get_SPCFileName","ICEnroll4::put_SPCFileName","ICEnroll::get_SPCFileName","ICEnroll::put_SPCFileName","SPCFileName property [Security]","SPCFileName property [Security]","CEnroll object","SPCFileName property [Security]","ICEnroll interface","SPCFileName property [Security]","ICEnroll2 interface","SPCFileName property [Security]","ICEnroll3 interface","SPCFileName property [Security]","ICEnroll4 interface","get_SPCFileName","security.icenroll4_spcfilename","xenroll/ICEnroll2::SPCFileName","xenroll/ICEnroll2::get_SPCFileName","xenroll/ICEnroll2::put_SPCFileName","xenroll/ICEnroll3::SPCFileName","xenroll/ICEnroll3::get_SPCFileName","xenroll/ICEnroll3::put_SPCFileName","xenroll/ICEnroll4::SPCFileName","xenroll/ICEnroll4::get_SPCFileName","xenroll/ICEnroll4::put_SPCFileName","xenroll/ICEnroll::SPCFileName","xenroll/ICEnroll::get_SPCFileName","xenroll/ICEnroll::put_SPCFileName"]
old-location: security\icenroll4_spcfilename.htm
tech.root: security
ms.assetid: 4ff2f111-31bd-4ed4-a335-2db536477660
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],SPCFileName property, ICEnroll interface [Security],SPCFileName property, ICEnroll.SPCFileName, ICEnroll.get_SPCFileName, ICEnroll2 interface [Security],SPCFileName property, ICEnroll2.SPCFileName, ICEnroll2::get_SPCFileName, ICEnroll2::put_SPCFileName, ICEnroll3 interface [Security],SPCFileName property, ICEnroll3.SPCFileName, ICEnroll3::get_SPCFileName, ICEnroll3::put_SPCFileName, ICEnroll4 interface [Security],SPCFileName property, ICEnroll4.SPCFileName, ICEnroll4::SPCFileName, ICEnroll4::get_SPCFileName, ICEnroll4::put_SPCFileName, ICEnroll::get_SPCFileName, ICEnroll::put_SPCFileName, SPCFileName property [Security], SPCFileName property [Security],CEnroll object, SPCFileName property [Security],ICEnroll interface, SPCFileName property [Security],ICEnroll2 interface, SPCFileName property [Security],ICEnroll3 interface, SPCFileName property [Security],ICEnroll4 interface, get_SPCFileName, security.icenroll4_spcfilename, xenroll/ICEnroll2::SPCFileName, xenroll/ICEnroll2::get_SPCFileName, xenroll/ICEnroll2::put_SPCFileName, xenroll/ICEnroll3::SPCFileName, xenroll/ICEnroll3::get_SPCFileName, xenroll/ICEnroll3::put_SPCFileName, xenroll/ICEnroll4::SPCFileName, xenroll/ICEnroll4::get_SPCFileName, xenroll/ICEnroll4::put_SPCFileName, xenroll/ICEnroll::SPCFileName, xenroll/ICEnroll::get_SPCFileName, xenroll/ICEnroll::put_SPCFileName
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
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICEnroll::get_SPCFileName
 - xenroll/ICEnroll::get_SPCFileName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - ICEnroll4.SPCFileName
 - ICEnroll4.get_SPCFileName
 - ICEnroll4.put_SPCFileName
 - ICEnroll3.SPCFileName
 - ICEnroll3.get_SPCFileName
 - ICEnroll3.put_SPCFileName
 - ICEnroll2.SPCFileName
 - ICEnroll2.get_SPCFileName
 - ICEnroll2.put_SPCFileName
 - ICEnroll.SPCFileName
 - ICEnroll.get_SPCFileName
 - ICEnroll.put_SPCFileName
 - CEnroll.SPCFileName
---

# ICEnroll::get_SPCFileName


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>SPCFileName</b> property sets or retrieves the name of the file to which to write the base64-encoded PKCS #7 (in <b>BSTR</b> form) as returned from the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a>.

This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a> interface.

This property is read/write.

## -parameters

## -remarks

The file is written as a binary PKCS #7. Specifying this file does not affect the acceptance of the certificates into any of the user's stores.

If the file already exists, the user is notified and prompted for permission to overwrite it.


<b>SPCFileName</b> affects the behavior of the following methods:

<ul>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-acceptpkcs7">acceptPKCS7</a>
</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-acceptfilepkcs7">acceptFilePKCS7</a>
</li>
</ul>



#### Examples


```cpp
BSTR     bstrSPCFile = NULL;
BSTR     bstrNewSPCFile = NULL;
HRESULT  hr;

// pEnroll is previously instantiated ICEnroll interface pointer

// get the SPCFileName
hr = pEnroll->get_SPCFileName( &bstrSPCFile );
if (FAILED( hr ))
    printf("Failed get_SPCFileName - %x\n", hr );
else
    printf( "SPCFileName: %ws\n", bstrSPCFile );
// free BSTR when done
if ( NULL != bstrSPCFile )
    SysFreeString( bstrSPCFile );

// set the SPCFileName, for example, "MyFile.SPC".
bstrNewSPCFile = SysAllocString(TEXT("<FILENAMEHERE>"));

hr = pEnroll->put_SPCFileName( bstrNewSPCFile );
if (FAILED( hr ))
    printf("Failed put_SPCFileName - %x\n", hr );
else
    printf( "SPCFileName set to %ws\n", bstrNewSPCFile );
// free BSTR when done
if ( NULL != bstrNewSPCFile )
    SysFreeString( bstrNewSPCFile );
```
