---
UID: NF:vfw.ICCompressorFree
title: ICCompressorFree function (vfw.h)
author: windows-sdk-content
description: The ICCompressorFree function frees the resources in the COMPVARS structure used by other VCM functions.
old-location: multimedia\iccompressorfree.htm
tech.root: Multimedia
ms.assetid: 6d0c9a7d-6458-4330-af74-3f471555cbfc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICCompressorFree, ICCompressorFree function [Windows Multimedia], _win32_ICCompressorFree, multimedia.iccompressorfree, vfw/ICCompressorFree
ms.topic: function
f1_keywords: 
 - "vfw/ICCompressorFree"
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Vfw32.lib
req.dll: Msvfw32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msvfw32.dll
api_name:
 - ICCompressorFree
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICCompressorFree function


## -description



The <b>ICCompressorFree</b> function frees the resources in the <a href="https://docs.microsoft.com/windows/desktop/api/vfw/ns-vfw-compvars">COMPVARS</a> structure used by other VCM functions.




## -parameters




### -param pc

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/vfw/ns-vfw-compvars">COMPVARS</a> structure containing the resources to be freed.


## -returns



This function does not return a value.




## -remarks



Use this function to release the resources in the <a href="https://docs.microsoft.com/windows/desktop/api/vfw/ns-vfw-compvars">COMPVARS</a> structure after using the <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-iccompressorchoose">ICCompressorChoose</a>, <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-icseqcompressframestart">ICSeqCompressFrameStart</a>, <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-icseqcompressframe">ICSeqCompressFrame</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-icseqcompressframeend">ICSeqCompressFrameEnd</a> functions.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-compression-functions">Video Compression Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
 

 

