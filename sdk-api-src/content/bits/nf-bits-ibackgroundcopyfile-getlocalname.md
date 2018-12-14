---
UID: NF:bits.IBackgroundCopyFile.GetLocalName
title: IBackgroundCopyFile::GetLocalName
author: windows-sdk-content
description: Retrieves the local name of the file.
old-location: bits\ibackgroundcopyfile_getlocalname.htm
tech.root: bits
ms.assetid: d27844b7-a5c6-4f4c-a1db-80e031898634
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetLocalName, GetLocalName method [BITS], GetLocalName method [BITS],IBackgroundCopyFile interface, IBackgroundCopyFile interface [BITS],GetLocalName method, IBackgroundCopyFile.GetLocalName, IBackgroundCopyFile::GetLocalName, _drz_ibackgroundcopyfile_getlocalname, bits.ibackgroundcopyfile_getlocalname, bits/IBackgroundCopyFile::GetLocalName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyFile.GetLocalName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyFile::GetLocalName


## -description


Retrieves the local name of the file.


## -parameters




### -param pVal [out]

Null-terminated string that contains the name of the file on the client. The name is fully qualified. Call the 
<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function to free <i>ppName</i> when done.


## -returns



This method returns <b>S_OK</b> on success or one of the standard COM <b>HRESULT</b> values on error.




## -remarks



The local file name is set when you call the 
<a href="https://msdn.microsoft.com/0dada1d3-49b6-41af-b17f-612f27ea4d56">AddFile</a> or 
<a href="https://msdn.microsoft.com/fe2f9b47-0f0a-48ab-be0e-658307cfec5f">AddFileSet</a> methods of the 
<a href="https://msdn.microsoft.com/91dd1ae1-1740-4d95-a476-fc18aead1dc2">IBackgroundCopyJob</a> interface.


#### Examples

The following example shows how to retrieve the local and remote file names and progress-related information from the  
<a href="https://msdn.microsoft.com/fae9cf56-c211-445b-b962-9a9d7d67c59c">IBackgroundCopyFile</a> interface. The example assumes the 
<b>IBackgroundCopyFile</b> interface pointer is valid.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IBackgroundCopyFile* pFile;
HRESULT hr;
WCHAR* pszLocalFileName = NULL;
WCHAR* pszRemoteFileName = NULL;
WCHAR  szPercentComplete[4+1];
BG_FILE_PROGRESS Progress;

hr = pFile-&gt;GetLocalName(&amp;pszLocalFileName);
if (SUCCEEDED(hr))
{
  hr = pFile-&gt;GetRemoteName(&amp;pszRemoteFileName);
  if (SUCCEEDED(hr))
  {
    pFile-&gt;GetProgress(&amp;Progress);
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
  CoTaskMemFree(pszRemoteFileName);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/fae9cf56-c211-445b-b962-9a9d7d67c59c">IBackgroundCopyFile</a>



<a href="https://msdn.microsoft.com/b6b1b1dc-776e-4369-bd39-d159e4edfe38">IBackgroundCopyFile::GetRemoteName</a>



<a href="https://msdn.microsoft.com/0dada1d3-49b6-41af-b17f-612f27ea4d56">IBackgroundCopyJob::AddFile</a>



<a href="https://msdn.microsoft.com/fe2f9b47-0f0a-48ab-be0e-658307cfec5f">IBackgroundCopyJob::AddFileSet</a>
 

 

