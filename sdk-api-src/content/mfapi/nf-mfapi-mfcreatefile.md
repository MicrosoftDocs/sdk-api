---
UID: NF:mfapi.MFCreateFile
title: MFCreateFile function (mfapi.h)

description: Creates a byte stream from a file.
old-location: mf\mfcreatefile.htm
tech.root: medfound
ms.assetid: 29269ea4-151f-4819-ae49-9f1c13a901e5

ms.date: 12/05/2018
ms.keywords: 29269ea4-151f-4819-ae49-9f1c13a901e5, MFCreateFile, MFCreateFile function [Media Foundation], mf.mfcreatefile, mfapi/MFCreateFile
ms.topic: function
f1_keywords: 
 - "mfapi/MFCreateFile"
dev_langs:
 - c++
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - MFCreateFile
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFCreateFile function


## -description


Creates a byte stream from a file.
        


## -parameters




### -param AccessMode

The requested access mode, specified as a member of the <a href="https://docs.microsoft.com/windows/win32/api/mfobjects/ne-mfobjects-mf_file_accessmode">MF_FILE_ACCESSMODE</a> enumeration.
          


### -param OpenMode

The behavior of the function if the file already exists or does not exist, specified as a member of the <a href="https://docs.microsoft.com/windows/win32/api/mfobjects/ne-mfobjects-mf_file_openmode">MF_FILE_OPENMODE</a> enumeration.
          


### -param fFlags

Bitwise <b>OR</b> of values from the <a href="https://docs.microsoft.com/windows/win32/api/mfobjects/ne-mfobjects-mf_file_flags">MF_FILE_FLAGS</a> enumeration.
          


### -param pwszFileURL

Pointer to a null-terminated string that contains the file name.
          


### -param ppIByteStream

Receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> interface of the byte stream. The caller must release the interface.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
 

 

