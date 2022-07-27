---
UID: NF:xenroll.ICEnroll.get_PVKFileName
title: ICEnroll::get_PVKFileName (xenroll.h)
description: The PVKFileName property of ICEnroll4 sets or retrieves the name of the file that will contain exported keys. (Get)
helpviewer_keywords: ["CEnroll object [Security]","PVKFileName property","ICEnroll interface [Security]","PVKFileName property","ICEnroll.PVKFileName","ICEnroll.get_PVKFileName","ICEnroll2 interface [Security]","PVKFileName property","ICEnroll2.PVKFileName","ICEnroll2::get_PVKFileName","ICEnroll2::put_PVKFileName","ICEnroll3 interface [Security]","PVKFileName property","ICEnroll3.PVKFileName","ICEnroll3::get_PVKFileName","ICEnroll3::put_PVKFileName","ICEnroll4 interface [Security]","PVKFileName property","ICEnroll4.PVKFileName","ICEnroll4::PVKFileName","ICEnroll4::get_PVKFileName","ICEnroll4::put_PVKFileName","ICEnroll::get_PVKFileName","ICEnroll::put_PVKFileName","PVKFileName property [Security]","PVKFileName property [Security]","CEnroll object","PVKFileName property [Security]","ICEnroll interface","PVKFileName property [Security]","ICEnroll2 interface","PVKFileName property [Security]","ICEnroll3 interface","PVKFileName property [Security]","ICEnroll4 interface","get_PVKFileName","security.icenroll4_pvkfilename","xenroll/ICEnroll2::PVKFileName","xenroll/ICEnroll2::get_PVKFileName","xenroll/ICEnroll2::put_PVKFileName","xenroll/ICEnroll3::PVKFileName","xenroll/ICEnroll3::get_PVKFileName","xenroll/ICEnroll3::put_PVKFileName","xenroll/ICEnroll4::PVKFileName","xenroll/ICEnroll4::get_PVKFileName","xenroll/ICEnroll4::put_PVKFileName","xenroll/ICEnroll::PVKFileName","xenroll/ICEnroll::get_PVKFileName","xenroll/ICEnroll::put_PVKFileName"]
old-location: security\icenroll4_pvkfilename.htm
tech.root: security
ms.assetid: 3f841bb2-6cfd-4712-bb71-5c3d9d462fab
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],PVKFileName property, ICEnroll interface [Security],PVKFileName property, ICEnroll.PVKFileName, ICEnroll.get_PVKFileName, ICEnroll2 interface [Security],PVKFileName property, ICEnroll2.PVKFileName, ICEnroll2::get_PVKFileName, ICEnroll2::put_PVKFileName, ICEnroll3 interface [Security],PVKFileName property, ICEnroll3.PVKFileName, ICEnroll3::get_PVKFileName, ICEnroll3::put_PVKFileName, ICEnroll4 interface [Security],PVKFileName property, ICEnroll4.PVKFileName, ICEnroll4::PVKFileName, ICEnroll4::get_PVKFileName, ICEnroll4::put_PVKFileName, ICEnroll::get_PVKFileName, ICEnroll::put_PVKFileName, PVKFileName property [Security], PVKFileName property [Security],CEnroll object, PVKFileName property [Security],ICEnroll interface, PVKFileName property [Security],ICEnroll2 interface, PVKFileName property [Security],ICEnroll3 interface, PVKFileName property [Security],ICEnroll4 interface, get_PVKFileName, security.icenroll4_pvkfilename, xenroll/ICEnroll2::PVKFileName, xenroll/ICEnroll2::get_PVKFileName, xenroll/ICEnroll2::put_PVKFileName, xenroll/ICEnroll3::PVKFileName, xenroll/ICEnroll3::get_PVKFileName, xenroll/ICEnroll3::put_PVKFileName, xenroll/ICEnroll4::PVKFileName, xenroll/ICEnroll4::get_PVKFileName, xenroll/ICEnroll4::put_PVKFileName, xenroll/ICEnroll::PVKFileName, xenroll/ICEnroll::get_PVKFileName, xenroll/ICEnroll::put_PVKFileName
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
 - ICEnroll::get_PVKFileName
 - xenroll/ICEnroll::get_PVKFileName
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
 - ICEnroll4.PVKFileName
 - ICEnroll4.get_PVKFileName
 - ICEnroll4.put_PVKFileName
 - ICEnroll3.PVKFileName
 - ICEnroll3.get_PVKFileName
 - ICEnroll3.put_PVKFileName
 - ICEnroll2.PVKFileName
 - ICEnroll2.get_PVKFileName
 - ICEnroll2.put_PVKFileName
 - ICEnroll.PVKFileName
 - ICEnroll.get_PVKFileName
 - ICEnroll.put_PVKFileName
 - CEnroll.PVKFileName
---

# ICEnroll::get_PVKFileName


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>PVKFileName</b> property sets or retrieves the name of the file that will contain exported keys.

This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a> interface.

This property is read/write.

## -parameters

## -remarks

The <b>PVKFileName</b> property affects the behavior of the following methods:

<ul>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-createpkcs10">createPKCS10</a>
</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-createfilepkcs10">createFilePKCS10</a>
</li>
</ul>


Exporting functionality may not be supported by the  <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP). Historically, <a href="/windows/desktop/SecGloss/a-gly">Authenticode</a> has exported the <a href="/windows/desktop/SecGloss/p-gly">private key</a> to a .pvk file on a disk and removed the keys from the registry. By default, private keys are not generated for exportation, and many cryptographic service providers do not support exporting keys. However, if the CSP supports exporting private keys, specifying a non-NULL value for the <b>PVKFileName</b> property causes the private keys to be generated as exportable and the private and public keys to be written to the file specified by the <b>PVKFileName</b> property. The private key is removed from the CSP. The file name specified by the property can be any accessible file. By default, no .pvk file is generated, and the keys are not generated as exportable.

If the .pvk file already exists, the user is notified and prompted for permission to overwrite it.


The 
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_genkeyflags">GenKeyFlags</a> property also has a flag that controls whether the private key can be exported. Use care when using  the <b>GenKeyFlags</b> property and the <b>PVKFileName</b> property together. If the <b>PVKFileName</b> property is set first, the <b>GenKeyFlags</b> property is automatically set to CRYPT_EXPORTABLE. If the <b>GenKeyFlags</b> property is set (by using the <b>put_GenKeyFlags</b> function) without including the CRYPT_EXPORTABLE flag, then the <b>GenKeyFlags</b> will not be set to CRYPT_EXPORTABLE, and the generated keys will not be exportable. The following procedure demonstrates this:

<ol>
<li>Call <b>put_PVKFileName</b> to set the file name for the file that will receive the exported keys. The <a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_genkeyflags">GenKeyFlags</a> property is automatically set to CRYPT_EXPORTABLE.</li>
<li>Call <b>put_GenKeyFlags</b> with a value not set to CRYPT_EXPORTABLE, for example, zero.</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_genkeyflags">GenKeyFlags</a> is no longer set to CRYPT_EXPORTABLE (the value that was automatically set in step one).</li>
</ol>


Any keys generated by following the previous steps will be not exportable. Therefore, it is recommended that the user set the <a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_genkeyflags">GenKeyFlags</a> property before the <b>PVKFileName</b> property when they are used together.

Alternatively, the user could determine the current value of the CRYPT_EXPORTABLE bit in the <a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_genkeyflags">GenKeyFlags</a> property and then perform a bitwise-<b>OR</b> operation between this value and any changes that are made to the <b>GenKeyFlags</b> property to ensure that the bit is not wiped out. The user could also specifically set the CRYPT_EXPORTABLE bit when updating the <b>GenKeyFlags</b> property.


#### Examples


```cpp
BSTR     bstrPVKFile = NULL;
BSTR     bstrNewPVKFile = NULL;
HRESULT  hr;

// pEnroll is previously instantiated ICEnroll interface pointer

// get the PVKFileName
hr = pEnroll->get_PVKFileName( &bstrPVKFile );
if (FAILED( hr ))
    printf("Failed get_PVKFileName - %x\n", hr );
else
    printf( "PVKFileName: %ws\n", bstrPVKFile );
// free BSTR when done
if ( NULL != bstrPVKFile )
    SysFreeString( bstrPVKFile );

// set the PVKFileName, for example, "MyKeys.pvk"
bstrNewPVKFile = SysAllocString(TEXT("FILENAMEHERE"));

hr = pEnroll->put_PVKFileName( bstrNewPVKFile );
if (FAILED( hr ))
    printf("Failed put_PVKFileName - %x\n", hr );
else
    printf( "PVKFileName set to %ws\n", bstrNewPVKFile );
// free BSTR when done
if ( NULL != bstrNewPVKFile )
    SysFreeString( bstrNewPVKFile );
```
