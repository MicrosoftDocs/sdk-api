---
UID: NF:xenroll.ICEnroll3.put_ReuseHardwareKeyIfUnableToGenNew
title: ICEnroll3::put_ReuseHardwareKeyIfUnableToGenNew (xenroll.h)
description: Sets or retrieves a Boolean value that determines the action taken by the certificate enrollment control object if an error is encountered when generating a new key. (Put)
helpviewer_keywords: ["CEnroll object [Security]","ReuseHardwareKeyIfUnableToGenNew property","ICEnroll3 interface [Security]","ReuseHardwareKeyIfUnableToGenNew property","ICEnroll3.ReuseHardwareKeyIfUnableToGenNew","ICEnroll3.put_ReuseHardwareKeyIfUnableToGenNew","ICEnroll3::get_ReuseHardwareKeyIfUnableToGenNew","ICEnroll3::put_ReuseHardwareKeyIfUnableToGenNew","ICEnroll4 interface [Security]","ReuseHardwareKeyIfUnableToGenNew property","ICEnroll4.ReuseHardwareKeyIfUnableToGenNew","ICEnroll4::ReuseHardwareKeyIfUnableToGenNew","ICEnroll4::get_ReuseHardwareKeyIfUnableToGenNew","ICEnroll4::put_ReuseHardwareKeyIfUnableToGenNew","ReuseHardwareKeyIfUnableToGenNew property [Security]","ReuseHardwareKeyIfUnableToGenNew property [Security]","CEnroll object","ReuseHardwareKeyIfUnableToGenNew property [Security]","ICEnroll3 interface","ReuseHardwareKeyIfUnableToGenNew property [Security]","ICEnroll4 interface","put_ReuseHardwareKeyIfUnableToGenNew","security.icenroll4_reusehardwarekeyifunabletogennew","xenroll/ICEnroll3::ReuseHardwareKeyIfUnableToGenNew","xenroll/ICEnroll3::get_ReuseHardwareKeyIfUnableToGenNew","xenroll/ICEnroll3::put_ReuseHardwareKeyIfUnableToGenNew","xenroll/ICEnroll4::ReuseHardwareKeyIfUnableToGenNew","xenroll/ICEnroll4::get_ReuseHardwareKeyIfUnableToGenNew","xenroll/ICEnroll4::put_ReuseHardwareKeyIfUnableToGenNew"]
old-location: security\icenroll4_reusehardwarekeyifunabletogennew.htm
tech.root: security
ms.assetid: 5a9d5f78-bf88-4e24-9685-7c504f9f2e38
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],ReuseHardwareKeyIfUnableToGenNew property, ICEnroll3 interface [Security],ReuseHardwareKeyIfUnableToGenNew property, ICEnroll3.ReuseHardwareKeyIfUnableToGenNew, ICEnroll3.put_ReuseHardwareKeyIfUnableToGenNew, ICEnroll3::get_ReuseHardwareKeyIfUnableToGenNew, ICEnroll3::put_ReuseHardwareKeyIfUnableToGenNew, ICEnroll4 interface [Security],ReuseHardwareKeyIfUnableToGenNew property, ICEnroll4.ReuseHardwareKeyIfUnableToGenNew, ICEnroll4::ReuseHardwareKeyIfUnableToGenNew, ICEnroll4::get_ReuseHardwareKeyIfUnableToGenNew, ICEnroll4::put_ReuseHardwareKeyIfUnableToGenNew, ReuseHardwareKeyIfUnableToGenNew property [Security], ReuseHardwareKeyIfUnableToGenNew property [Security],CEnroll object, ReuseHardwareKeyIfUnableToGenNew property [Security],ICEnroll3 interface, ReuseHardwareKeyIfUnableToGenNew property [Security],ICEnroll4 interface, put_ReuseHardwareKeyIfUnableToGenNew, security.icenroll4_reusehardwarekeyifunabletogennew, xenroll/ICEnroll3::ReuseHardwareKeyIfUnableToGenNew, xenroll/ICEnroll3::get_ReuseHardwareKeyIfUnableToGenNew, xenroll/ICEnroll3::put_ReuseHardwareKeyIfUnableToGenNew, xenroll/ICEnroll4::ReuseHardwareKeyIfUnableToGenNew, xenroll/ICEnroll4::get_ReuseHardwareKeyIfUnableToGenNew, xenroll/ICEnroll4::put_ReuseHardwareKeyIfUnableToGenNew
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
 - ICEnroll3::put_ReuseHardwareKeyIfUnableToGenNew
 - xenroll/ICEnroll3::put_ReuseHardwareKeyIfUnableToGenNew
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
 - ICEnroll4.ReuseHardwareKeyIfUnableToGenNew
 - ICEnroll4.get_ReuseHardwareKeyIfUnableToGenNew
 - ICEnroll4.put_ReuseHardwareKeyIfUnableToGenNew
 - ICEnroll3.ReuseHardwareKeyIfUnableToGenNew
 - ICEnroll3.get_ReuseHardwareKeyIfUnableToGenNew
 - ICEnroll3.put_ReuseHardwareKeyIfUnableToGenNew
 - CEnroll.ReuseHardwareKeyIfUnableToGenNew
---

# ICEnroll3::put_ReuseHardwareKeyIfUnableToGenNew


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>ReuseHardwareKeyIfUnableToGenNew</b> property sets or retrieves a Boolean value that determines the action taken by the 
certificate enrollment control object if an error is encountered when generating a new key.

This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll3">ICEnroll3</a> interface.

This property is read/write.

## -parameters

## -remarks

This property is a Boolean value. This property affects only <a href="/windows/desktop/SecGloss/c-gly">cryptographic service providers</a> that return NTE_TOKEN_KEYSET_STORAGE_FULL. These CSPs are typically hardware-based; an example is a smart card. If this property is true and an error is encountered while generating a new key, the certificate enrollment control object will reuse the existing hardware key. If this property is false and an error is encountered while generating a new key, the certificate enrollment control object will not reuse the existing hardware key but will instead pass an error to the caller.


#### Examples


```cpp
// Code to set the reuse H/W key status.
// hr is HRESULT variable.
hr = pEnroll->put_ReuseHardwareKeyIfUnableToGenNew( FALSE );
if ( FAILED( hr ) )    
    printf("Failed put_ReuseHardwareKeyIfUnableToGenNew [%x]\n", hr);


// Code to retrieve the reuse H/W key status.
BOOL bReuse;

hr = pEnroll->get_ReuseHardwareKeyIfUnableToGenNew( &bReuse );
if ( FAILED( hr ) )
    printf("Failed get_ReuseHardwareKeyIfUnableToGenNew [%x]\n", hr);
else
    printf("Hardware key %s be reused if unable"
        " to generate a new key.\n", bReuse ? "will" : "will not");
```

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa376007(v=vs.85)">CEnroll</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll3">ICEnroll3</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a>
