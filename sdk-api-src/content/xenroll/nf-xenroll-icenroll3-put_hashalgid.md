---
UID: NF:xenroll.ICEnroll3.put_HashAlgID
title: ICEnroll3::put_HashAlgID
author: windows-sdk-content
description: Sets or retrieves the hash algorithm used when signing a PKCS #10 certificate request.
old-location: security\icenroll4_hashalgid.htm
tech.root: seccrypto
ms.assetid: 46f371a3-7254-4f54-b147-402f2a37e277
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: CEnroll object [Security],HashAlgID property, HashAlgID property [Security], HashAlgID property [Security],CEnroll object, HashAlgID property [Security],ICEnroll3 interface, HashAlgID property [Security],ICEnroll4 interface, ICEnroll3 interface [Security],HashAlgID property, ICEnroll3.HashAlgID, ICEnroll3.put_HashAlgID, ICEnroll3::get_HashAlgID, ICEnroll3::put_HashAlgID, ICEnroll4 interface [Security],HashAlgID property, ICEnroll4.HashAlgID, ICEnroll4::HashAlgID, ICEnroll4::get_HashAlgID, ICEnroll4::put_HashAlgID, put_HashAlgID, security.icenroll4_hashalgid, xenroll/ICEnroll3::HashAlgID, xenroll/ICEnroll3::get_HashAlgID, xenroll/ICEnroll3::put_HashAlgID, xenroll/ICEnroll4::HashAlgID, xenroll/ICEnroll4::get_HashAlgID, xenroll/ICEnroll4::put_HashAlgID
ms.prod: windows-hardware
ms.technology: windows-devices
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICEnroll3::put_HashAlgID


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>HashAlgID</b> property sets or retrieves the <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash algorithm</a> used when signing a PKCS #10 <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a>.

This property was first introduced in the <a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a> interface.

This property is read/write.


## -parameters


## -remarks



The values for this property are <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash algorithm</a> IDs, such as those returned by the 
<a href="https://msdn.microsoft.com/b7fe4abc-38e8-42a0-a7a0-312ccfc309e5">EnumAlgs</a> method. If both the <b>HashAlgID</b> and 
<a href="https://msdn.microsoft.com/48f8a47b-0ab4-4150-b8cf-37e57fb04d3e">HashAlgorithm</a> properties are set, whichever has been updated most recently determines the hash algorithm used to sign the PKCS #10 request.


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




<a href="https://msdn.microsoft.com/7f13549d-811b-496b-abdd-7e52cbc2ed54">CEnroll</a>



<a href="https://msdn.microsoft.com/b7fe4abc-38e8-42a0-a7a0-312ccfc309e5">EnumAlgs</a>



<a href="https://msdn.microsoft.com/48f8a47b-0ab4-4150-b8cf-37e57fb04d3e">HashAlgorithm</a>



<a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>



<a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a>
 

 

