---
UID: NF:shobjidl_core.IShellLibrary.Save
title: IShellLibrary::Save
author: windows-sdk-content
description: Saves the library to a new Library Description (*.library-ms) file.
old-location: shell\IShellLibrary_Save.htm
old-project: shell
ms.assetid: 2a7de829-f0bc-4ace-aed4-83d0611ae292
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IShellLibrary interface [Windows Shell],Save method, IShellLibrary.Save, IShellLibrary::Save, Save, Save method [Windows Shell], Save method [Windows Shell],IShellLibrary interface, _shell_IShellLibrary_Save, shell.IShellLibrary_Save, shobjidl_core/IShellLibrary::Save
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IShellLibrary.Save
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IShellLibrary::Save


## -description


Saves the library to a new Library Description (*.library-ms) file.


## -parameters




### -param psiFolderToSaveIn [in]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>*</b>

The  <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> object  that specifies the folder in which to save the library, or <b>NULL</b> to save the library  with the user's default libraries in the FOLDERID_Libraries known folder.


### -param pszLibraryName [in]

Type: <b>LPCWSTR</b>

The file name under which to save the library. The file name must not include the file name extension; the file name extension is added automatically.


### -param lsf [in]

Type: <b><a href="https://msdn.microsoft.com/cae52226-0030-457b-aebf-00aaf860243d">LIBRARYSAVEFLAGS</a></b>

The <a href="https://msdn.microsoft.com/cae52226-0030-457b-aebf-00aaf860243d">LIBRARYSAVEFLAGS</a>  value that specifies how to handle a library name collision.


### -param ppsiSavedTo [out]

Type: <b><a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>**</b>

The  <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> object  that represents the library description file into   which the library was saved.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>IShellLibrary::Save</b> and <a href="https://msdn.microsoft.com/953b209b-fd18-49d0-84d3-ad9b815f2a3a">SHSaveLibraryInFolderPath</a> create a new library file, and save the file to disk. To save changes made to a library that has an existing library file, call  <a href="https://msdn.microsoft.com/a340964d-ea20-4a3b-be8b-f4f4dbf624ed">IShellLibrary::Commit</a>.

If the library is saved in the Libraries known folder (FOLDERID_Libraries), the library's location is automatically added to the system index.

For convenience, <a href="https://msdn.microsoft.com/953b209b-fd18-49d0-84d3-ad9b815f2a3a">SHSaveLibraryInFolderPath</a> can be used in place of this method.


#### Examples

The following code example shows the helper function <a href="https://msdn.microsoft.com/953b209b-fd18-49d0-84d3-ad9b815f2a3a">SHSaveLibraryInFolderPath</a>, which wraps this method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//
// from shobjidl.h
//
__inline HRESULT SHSaveLibraryInFolderPath(
    __in IShellLibrary *plib, 
    __in PCWSTR pszFolderPath, 
    __in PCWSTR pszLibraryName, 
    __in LIBRARYSAVEFLAGS lsf, 
    __deref_opt_out PWSTR *ppszSavedToPath
)
{
    if (ppszSavedToPath)
    {
        *ppszSavedToPath = NULL;
    }

    IShellItem *psiFolder;
    HRESULT hr = SHCreateItemFromParsingName(
      pszFolderPath, 
      NULL, 
      IID_PPV_ARGS(&amp;psiFolder));

    if (SUCCEEDED(hr))
    {
        IShellItem *psiSavedTo;
        hr = plib-&gt;Save(psiFolder, pszLibraryName, lsf, &amp;psiSavedTo);

        if (SUCCEEDED(hr))
        {
            if (ppszSavedToPath)
            {
                hr = psiSavedTo-&gt;GetDisplayName(
                  SIGDN_DESKTOPABSOLUTEPARSING, 
                  ppszSavedToPath);
            }
            psiSavedTo-&gt;Release();
        }
        psiFolder-&gt;Release();
    }
    return hr;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/c1ef3d22-7c88-42b0-93a2-5d1b75c327ba">IShellLibrary</a>



<a href="https://msdn.microsoft.com/953b209b-fd18-49d0-84d3-ad9b815f2a3a">SHSaveLibraryInFolderPath</a>



<a href="https://msdn.microsoft.com/19DA68B2-FCB6-443d-A3CD-0BF2F429B149">Windows Libraries</a>
 

 

