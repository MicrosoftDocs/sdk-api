---
UID: NF:bits.IBackgroundCopyFile.GetLocalName
title: IBackgroundCopyFile::GetLocalName (bits.h)
description: Retrieves the local name of the file.
helpviewer_keywords: ["GetLocalName","GetLocalName method [BITS]","GetLocalName method [BITS]","IBackgroundCopyFile interface","IBackgroundCopyFile interface [BITS]","GetLocalName method","IBackgroundCopyFile.GetLocalName","IBackgroundCopyFile::GetLocalName","_drz_ibackgroundcopyfile_getlocalname","bits.ibackgroundcopyfile_getlocalname","bits/IBackgroundCopyFile::GetLocalName"]
old-location: bits\ibackgroundcopyfile_getlocalname.htm
tech.root: Bits
ms.assetid: d27844b7-a5c6-4f4c-a1db-80e031898634
ms.date: 12/05/2018
ms.keywords: GetLocalName, GetLocalName method [BITS], GetLocalName method [BITS],IBackgroundCopyFile interface, IBackgroundCopyFile interface [BITS],GetLocalName method, IBackgroundCopyFile.GetLocalName, IBackgroundCopyFile::GetLocalName, _drz_ibackgroundcopyfile_getlocalname, bits.ibackgroundcopyfile_getlocalname, bits/IBackgroundCopyFile::GetLocalName
req.header: bits.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyFile::GetLocalName
 - bits/IBackgroundCopyFile::GetLocalName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyFile.GetLocalName
---

# IBackgroundCopyFile::GetLocalName


## -description

Retrieves the local name of the file.

## -parameters

### -param pVal [out]

Null-terminated string that contains the name of the file on the client. The name is fully qualified. Call the 
<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free <i>ppName</i> when done.

## -returns

This method returns <b>S_OK</b> on success or one of the standard COM <b>HRESULT</b> values on error.

## -remarks

The local file name is set when you call the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-addfile">AddFile</a> or 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-addfileset">AddFileSet</a> methods of the 
<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyjob">IBackgroundCopyJob</a> interface.


#### Examples

The following example shows how to retrieve the local and remote file names and progress-related information from the  
<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyfile">IBackgroundCopyFile</a> interface. The example assumes the 
<b>IBackgroundCopyFile</b> interface pointer is valid.


```cpp
IBackgroundCopyFile* pFile;
HRESULT hr;
WCHAR* pszLocalFileName = NULL;
WCHAR* pszRemoteFileName = NULL;
WCHAR  szPercentComplete[4+1];
BG_FILE_PROGRESS Progress;

hr = pFile->GetLocalName(&pszLocalFileName);
if (SUCCEEDED(hr))
{
  hr = pFile->GetRemoteName(&pszRemoteFileName);
  if (SUCCEEDED(hr))
  {
    pFile->GetProgress(&Progress);
    if (BG_SIZE_UNKNOWN == Progress.BytesTotal) 
    {
      StringCchPrintf(szPercentComplete, sizeof(szPercentComplete), L"0%%");
    } 
    else 
    {
      StringCchPrintf(szPercentComplete, sizeof(szPercentComplete), L"%I64d%%", 
          100*Progress.BytesTransferred/Progress.BytesTotal); 
    }
    //Do something with the file names and progress information.
  }
}
if (pszLocalFileName)
  CoTaskMemFree(pszLocalFileName);
if (pszRemoteFileName)
  CoTaskMemFree(pszRemoteFileName);
```

## -see-also

<a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyfile">IBackgroundCopyFile</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyfile-getremotename">IBackgroundCopyFile::GetRemoteName</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-addfile">IBackgroundCopyJob::AddFile</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-addfileset">IBackgroundCopyJob::AddFileSet</a>