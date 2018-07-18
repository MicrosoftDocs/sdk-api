---
UID: NF:commctrl.ImageList_ReadEx
title: ImageList_ReadEx function
author: windows-sdk-content
description: Reads an image list from a stream, and returns an IImageList interface to the image list.
old-location: controls\ImageList_ReadEx.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_readex.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: ILP_DOWNLEVEL, ILP_NORMAL, ImageList_ReadEx, ImageList_ReadEx function [Windows Controls], _win32_ImageList_ReadEx, _win32_ImageList_ReadEx_cpp, commctrl/ImageList_ReadEx, controls.ImageList_ReadEx, controls._win32_ImageList_ReadEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
tech.root: 
req.typenames: STGOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - ImageList_ReadEx
product: Windows
targetos: Windows
req.lib: Comctl32.lib
req.dll: Comctl32.dll (version 6.0 or later)
req.irql: 
---

# ImageList_ReadEx function


## -description



Reads an image list from a stream, and returns an <a href="https://msdn.microsoft.com/02e397a4-22fa-49fb-8103-376aa5ebc77a">IImageList</a> interface to the image list. 



## -parameters




### -param dwFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>


		A flag that specifies how the stream is read.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ILP_NORMAL"></a><a id="ilp_normal"></a><dl>
<dt><b>ILP_NORMAL</b></dt>
</dl>
</td>
<td width="60%">

			Expects an image list that was written with the ILP_NORMAL flag specified.
			

</td>
</tr>
<tr>
<td width="40%"><a id="ILP_DOWNLEVEL"></a><a id="ilp_downlevel"></a><dl>
<dt><b>ILP_DOWNLEVEL</b></dt>
</dl>
</td>
<td width="60%">

			Expects an image list that was written with the ILP_DOWNLEVEL flag specified.
			

</td>
</tr>
</table>
 


### -param pstm [in]

Type: <b>LPSTREAM</b>


		The address of the stream. 
		


### -param riid [out]

Type: <b>REFIID</b>


					An IID for the image list.
		


### -param ppv [out]

Type: <b>void**</b>


		The address of a pointer to the interface for the image list if successful, <b>NULL</b> otherwise.
		


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use <b>ImageList_ReadEx</b>, the application must specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 




## -see-also




<a href="https://msdn.microsoft.com/d0b6b9ca-18e5-4db5-8995-3db81adaec25">ImageList_Read</a>



<a href="https://msdn.microsoft.com/00078f34-3c8c-45dd-be81-9d62b90222ca">ImageList_Write</a>



<a href="https://msdn.microsoft.com/0cb345a9-4d6f-4218-ab70-26cf2ddeb2b3">ImageList_WriteEx</a>



<b>Reference</b>
 

 

