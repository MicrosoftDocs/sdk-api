---
UID: NF:vfw.IAVIFile.Info
title: IAVIFile::Info
author: windows-driver-content
description: The Info method returns with information about an AVI file. Called when an application uses the AVIFileInfo function.
old-location: multimedia\iavifile_info.htm
old-project: Multimedia
ms.assetid: cac01da4-b979-4386-8fc7-f47a7771e6f4
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: IAVIFile interface [Windows Multimedia],Info method, IAVIFile.Info, IAVIFile::Info, Info, Info method [Windows Multimedia], Info method [Windows Multimedia],IAVIFile interface, _win32_IAVIFile_Info, multimedia.iavifile_info, vfw/IAVIFile::Info
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: VS_FIXEDFILEINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Vfw32.lib
-	Vfw32.dll
api_name:
-	IAVIFile.Info
product: Windows
targetos: Windows
req.lib: Vfw32.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IAVIFile::Info


## -description



The <b>Info</b> method returns with information about an AVI file. Called when an application uses the <a href="https://msdn.microsoft.com/10d7decf-a133-4d55-93d5-867952307819">AVIFileInfo</a> function.




## -parameters




### -param pfi


            A pointer to an <a href="https://msdn.microsoft.com/d3fda342-2ade-41b1-b709-c194f132e015">AVIFILEINFO</a> structure. The method fills the structure with information about the file.


### -param lSize

The size, in bytes, of the buffer specified by <i>pfi</i>.


#### - pf


            Pointer to the interface to a file.
          


## -returns




            Returns the HRESULT defined by OLE.
          




## -remarks



If the buffer allocated is too small for the structure, this method should fail the call by returning AVIERR_BUFFERTOOSMALL. Otherwise, it should fill the structure and return its size.

For handlers written in C++, <b>Info</b> has the following syntax:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT Info(AVIFILEINFO *pfi, LONG lSize) 
 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ced6f7d1-5f27-47f4-a912-8c17ea5fa685">Custom File and Stream Handler Interfaces</a>



<a href="https://msdn.microsoft.com/c61e0118-d405-4c1e-9ae8-ed6a145a5d6b">Custom File and Stream Handlers</a>
 

 

