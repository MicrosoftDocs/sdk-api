---
UID: NF:mfapi.MFTRegisterLocalByCLSID
title: MFTRegisterLocalByCLSID function (mfapi.h)
author: windows-sdk-content
description: Registers a Media Foundation transform (MFT) in the caller's process.
old-location: mf\mftregisterlocalbyclsid.htm
tech.root: medfound
ms.assetid: 80c45ac3-4487-41bf-a5f5-f459db3cd700
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MFTRegisterLocalByCLSID, MFTRegisterLocalByCLSID function [Media Foundation], mf.mftregisterlocalbyclsid, mfapi/MFTRegisterLocalByCLSID
ms.topic: function
f1_keywords: 
 - "mfapi/MFTRegisterLocalByCLSID"
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
 - MFTRegisterLocalByCLSID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFTRegisterLocalByCLSID function


## -description


Registers a Media Foundation transform (MFT) in the caller's process.


## -parameters




### -param clisdMFT [in]

The class identifier (CLSID) of the MFT.


### -param guidCategory [in]

A GUID that specifies the category of the MFT. For a list of MFT categories, see <a href="https://docs.microsoft.com/windows/desktop/medfound/mft-category">MFT_CATEGORY</a>.


### -param pszName [in]

A wide-character null-terminated string that contains the friendly name of the MFT.


### -param Flags [in]

A bitwise <b>OR</b> of zero or more flags from the <a href="https://docs.microsoft.com/windows/win32/api/mfapi/ne-mfapi-_mft_enum_flag">_MFT_ENUM_FLAG</a> enumeration.


### -param cInputTypes [in]

The number of elements in the <i>pInputTypes</i> array.


### -param pInputTypes [in]

A pointer to an array of <a href="https://docs.microsoft.com/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info">MFT_REGISTER_TYPE_INFO</a> structures. Each member of the array specifies an input format that the MFT supports. This parameter can be <b>NULL</b> if <i>cInputTypes</i> is zero.


### -param cOutputTypes [in]

The number of elements in the <i>pOutputTypes</i> array.


### -param pOutputTypes [in]

A pointer to an array of <a href="https://docs.microsoft.com/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info">MFT_REGISTER_TYPE_INFO</a> structures. Each member of the array defines an output format that the MFT supports. This parameter can be <b>NULL</b> if <i>cOutputTypes</i> is zero.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The primary purpose of this function is to make an MFT available for automatic topology resolution without making the MFT available to other processes or applications.

After you call this function, the MFT can be enumerated by calling the <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mftenumex">MFTEnumEx</a> function with the <b>MFT_ENUM_FLAG_LOCALMFT</b> flag. The MFT can be enumerated from within the same process, but is not visible to other processes.

To unregister the MFT from the current process, call <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mftunregisterlocalbyclsid">MFTUnregisterLocalByCLSID</a>.

If you need to register an MFT in the Protected Media Path (PMP) process, use the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imflocalmftregistration">IMFLocalMFTRegistration</a> interface.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal">MFTRegisterLocal</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
 

 

