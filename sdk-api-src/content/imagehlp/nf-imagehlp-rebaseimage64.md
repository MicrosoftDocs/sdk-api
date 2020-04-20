---
UID: NF:imagehlp.ReBaseImage64
title: ReBaseImage64 function (imagehlp.h)
description: Changes the load address for the specified image, which reduces the required load time for a DLL.helpviewer_keywords: ["ReBaseImage64","ReBaseImage64 function","base.rebaseimage64","imagehlp/ReBaseImage64"]
old-location: base\rebaseimage64.htm
tech.root: Debug
ms.assetid: 3d60358c-8aa6-4b30-a46e-ce0e15964b5a
ms.date: 12/05/2018
ms.keywords: ReBaseImage64, ReBaseImage64 function, base.rebaseimage64, imagehlp/ReBaseImage64
f1_keywords:
- imagehlp/ReBaseImage64
dev_langs:
- c++
req.header: imagehlp.h
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
req.lib: Imagehlp.lib
req.dll: Imagehlp.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Imagehlp.dll
api_name:
- ReBaseImage64
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ReBaseImage64 function


## -description


Changes the load address for the specified image, which reduces the required load time for a DLL.

Alternatively, you can use the 
Rebase tool. This tool is available in Visual Studio and the <a href="https://msdn.microsoft.com/windowsserver/bb980924.aspx">Windows SDK</a>.


## -parameters




### -param CurrentImageName [in]

The name of the file to be rebased. You must specify the full path to the file unless the module is in the current working directory of the calling process.


### -param SymbolPath [in]

The path used to find the corresponding symbol file. Specify this path for executable images that have symbolic information because when image addresses change, the corresponding symbol database file (PDB) may also need to be changed.    Note that even if the symbol path is not valid, the function will succeed if it is able to rebases your image.


### -param fReBase [in]

If this value is <b>TRUE</b>, the image is rebased. Otherwise, the image is not rebased.


### -param fRebaseSysfileOk [in]

If this value is <b>TRUE</b>, the system image is rebased. Otherwise, the system image is not rebased.


### -param fGoingDown [in]

If this value is <b>TRUE</b>, the image can be rebased below the given base; otherwise, it cannot.


### -param CheckImageSize [in]

The maximum size that the image can grow to, in bytes, or zero if there is no limit.


### -param OldImageSize [out]

A pointer to a variable that receives the original image size, in bytes.


### -param OldImageBase [out]

A pointer to a variable that receives the original image base.


### -param NewImageSize [out]

A pointer to a variable that receives the new image size after the rebase operation, in bytes.


### -param NewImageBase [in, out]

The base address to use for rebasing the image. If the address is not available and the <i>fGoingDown</i> parameter is set to <b>TRUE</b>, the function finds a new base address and sets this parameter to the new base address. If <i>fGoingDown</i> is <b>FALSE</b>, the function finds a new base address but does not set this parameter to the new base address.


### -param TimeStamp [in]

The new time date stamp for the image file header. The value must be represented in the number of seconds elapsed since midnight (00:00:00), January 1, 1970, Universal Coordinated Time, according to the system clock.

If this parameter is 0, the current file header time date stamp is incremented by 1 second.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The 
<b>ReBaseImage64</b> function changes the desired load address for the specified image. This operation involves reading the entire image and updating all fixups, debugging information, and checksum. You can rebase an image to reduce the required load time for its DLLs. If an application can rely on a DLL being loaded at the desired load address, then the system loader does not have to relocate the image. The image is simply loaded into the application's virtual address space and the 
<a href="https://docs.microsoft.com/windows/desktop/Dlls/dllmain">DllMain</a> function is called, if one is present.

All ImageHlp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

You cannot rebase DLLs that link with /DYNAMICBASE or that reside in protected directories, such as the System32 folder.

As an alternative to using this function, see the <a href="https://msdn.microsoft.com/library/f7f5138s.aspx">/BASE</a> linker option.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Dlls/dllmain">DllMain</a>



<a href="https://docs.microsoft.com/windows/desktop/Debug/imagehlp-functions">ImageHlp Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imagehlp/nf-imagehlp-rebaseimage">ReBaseImage</a>
 

 

