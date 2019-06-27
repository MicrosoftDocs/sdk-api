---
UID: NF:mfapi.MFTRegisterLocal
title: MFTRegisterLocal function (mfapi.h)
author: windows-sdk-content
description: Registers a Media Foundation transform (MFT) in the caller's process.
old-location: mf\mftregisterlocal.htm
tech.root: medfound
ms.assetid: 802f7083-e224-4e5c-8a35-3e93da0cbd91
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MFTRegisterLocal, MFTRegisterLocal function [Media Foundation], mf.mftregisterlocal, mfapi/MFTRegisterLocal
ms.topic: function
f1_keywords: 
 - "mfapi/MFTRegisterLocal"
req.header: mfapi.h
req.include-header: 
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
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFTRegisterLocal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFTRegisterLocal function


## -description


Registers a Media Foundation transform (MFT) in the caller's process.


## -parameters




### -param pClassFactory [in]

A pointer to the <b>IClassFactory</b> interface of a class factory object. The class factory creates the MFT.


### -param guidCategory [in]

A GUID that specifies the category of the MFT. For a list of MFT categories, see <a href="https://docs.microsoft.com/windows/desktop/medfound/mft-category">MFT_CATEGORY</a>.


### -param pszName [in]

A wide-character null-terminated string that contains the friendly name of the MFT.


### -param Flags [in]

A bitwise <b>OR</b> of zero or more flags from the <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/ne-mfapi-_mft_enum_flag">_MFT_ENUM_FLAG</a> enumeration.


### -param cInputTypes [in]

The number of elements in the <i>pInputTypes</i> array.


### -param pInputTypes [in]

A pointer to an array of <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/ns-mfobjects-__midl___midl_itf_mfobjects_0000_0008_0003">MFT_REGISTER_TYPE_INFO</a> structures. Each member of the array specifies an input format that the MFT supports. This parameter can be <b>NULL</b> if <i>cInputTypes</i> is zero.


### -param cOutputTypes [in]

The number of elements in the <i>pOutputTypes</i> array.


### -param pOutputTypes [in]

A pointer to an array of <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/ns-mfobjects-__midl___midl_itf_mfobjects_0000_0008_0003">MFT_REGISTER_TYPE_INFO</a> structures. Each member of the array defines an output format that the MFT supports. This parameter can be <b>NULL</b> if <i>cOutputTypes</i> is zero.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The primary purpose of this function is to make an MFT available for automatic topology resolution without making the MFT available to other processes or applications.

After you call this function, the MFT can be enumerated by calling the <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mftenumex">MFTEnumEx</a> function with the <b>MFT_ENUM_FLAG_LOCALMFT</b> flag. The MFT can be enumerated from within the same process, but is not visible to other processes.

The <i>pClassFactory</i> parameter specifies a class factory object that creates the MFT. The class factory's <b>IClassFactory::CreateInstance</b> method must return an object that supports the <a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a> interface.

<div class="alert"><b>Note</b>  The <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mftenumex">MFTEnumEx</a> function retrieves a list of <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> pointers. However, the class factory does not need to support the <b>IMFActivate</b> interface. Instead, the <b>MFTEnumEx</b> function provides an implementation of <b>IMFActivate</b> that wraps the class factory.</div>
<div> </div>
To unregister the MFT from the current process, call <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mftunregisterlocal">MFTUnregisterLocal</a>.

If you need to register an MFT in the Protected Media Path (PMP) process, use the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imflocalmftregistration">IMFLocalMFTRegistration</a> interface.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid">MFTRegisterLocalByCLSID</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
 

 

