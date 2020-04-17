---
UID: NF:xenroll.ICEnroll3.get_HashAlgID
title: ICEnroll3::get_HashAlgID (xenroll.h)
description: Sets or retrieves the hash algorithm used when signing a PKCShelpviewer_keywords: ["CEnroll object [Security]","HashAlgID property","HashAlgID property [Security]","HashAlgID property [Security]","CEnroll object","HashAlgID property [Security]","ICEnroll3 interface","HashAlgID property [Security]","ICEnroll4 interface","ICEnroll3 interface [Security]","HashAlgID property","ICEnroll3.HashAlgID","ICEnroll3.get_HashAlgID","ICEnroll3::get_HashAlgID","ICEnroll3::put_HashAlgID","ICEnroll4 interface [Security]","HashAlgID property","ICEnroll4.HashAlgID","ICEnroll4::HashAlgID","ICEnroll4::get_HashAlgID","ICEnroll4::put_HashAlgID","get_HashAlgID","security.icenroll4_hashalgid","xenroll/ICEnroll3::HashAlgID","xenroll/ICEnroll3::get_HashAlgID","xenroll/ICEnroll3::put_HashAlgID","xenroll/ICEnroll4::HashAlgID","xenroll/ICEnroll4::get_HashAlgID","xenroll/ICEnroll4::put_HashAlgID"]
old-location: security\icenroll4_hashalgid.htm
tech.root: SecCrypto
ms.assetid: 46f371a3-7254-4f54-b147-402f2a37e277
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],HashAlgID property, HashAlgID property [Security], HashAlgID property [Security],CEnroll object, HashAlgID property [Security],ICEnroll3 interface, HashAlgID property [Security],ICEnroll4 interface, ICEnroll3 interface [Security],HashAlgID property, ICEnroll3.HashAlgID, ICEnroll3.get_HashAlgID, ICEnroll3::get_HashAlgID, ICEnroll3::put_HashAlgID, ICEnroll4 interface [Security],HashAlgID property, ICEnroll4.HashAlgID, ICEnroll4::HashAlgID, ICEnroll4::get_HashAlgID, ICEnroll4::put_HashAlgID, get_HashAlgID, security.icenroll4_hashalgid, xenroll/ICEnroll3::HashAlgID, xenroll/ICEnroll3::get_HashAlgID, xenroll/ICEnroll3::put_HashAlgID, xenroll/ICEnroll4::HashAlgID, xenroll/ICEnroll4::get_HashAlgID, xenroll/ICEnroll4::put_HashAlgID
f1_keywords:
- xenroll/ICEnroll4.HashAlgID
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Xenroll.dll
api_name:
- ICEnroll4.HashAlgID
- ICEnroll4.get_HashAlgID
- ICEnroll4.put_HashAlgID
- ICEnroll3.HashAlgID
- ICEnroll3.get_HashAlgID
- ICEnroll3.put_HashAlgID
- CEnroll.HashAlgID
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICEnroll3::get_HashAlgID


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>HashAlgID</b> property sets or retrieves the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/h-gly">hash algorithm</a> used when signing a PKCS #10 <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate request</a>.

This property was first introduced in the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll3">ICEnroll3</a> interface.

This property is read/write.


## -parameters


## -remarks



The values for this property are <a href="https://docs.microsoft.com/windows/desktop/SecGloss/h-gly">hash algorithm</a> IDs, such as those returned by the 
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll3-enumalgs">EnumAlgs</a> method. If both the <b>HashAlgID</b> and 
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_hashalgorithm">HashAlgorithm</a> properties are set, whichever has been updated most recently determines the hash algorithm used to sign the PKCS #10 request.


#### Examples


```cpp
// Code to set the hash algorithm ID.
// hr is HRESULT variable.
hr = pEnroll->put_HashAlgID( CALG_MD4 );
if ( FAILED( hr ) )    
    printf("Failed put_HashAlgID [%x]\n", hr);


// Code to retrieve the hash algorithm ID.
DWORD dwHashID;

hr = pEnroll->get_HashAlgID( &dwHashID );
if ( FAILED( hr ) )    
    printf("Failed get_HashAlgID [%x]\n", hr);
else
    printf("HashAlgID: %d\n", dwHashID);
```





## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa376007(v=vs.85)">CEnroll</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll3-enumalgs">EnumAlgs</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_hashalgorithm">HashAlgorithm</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll3">ICEnroll3</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a>
 

 

