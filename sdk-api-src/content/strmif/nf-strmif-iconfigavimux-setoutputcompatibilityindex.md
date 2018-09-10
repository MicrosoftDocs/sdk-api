---
UID: NF:strmif.IConfigAviMux.SetOutputCompatibilityIndex
title: IConfigAviMux::SetOutputCompatibilityIndex
author: windows-sdk-content
description: The SetOutputCompatibilityIndex method sets the AVI index format.
old-location: dshow\iconfigavimux_setoutputcompatibilityindex.htm
tech.root: DirectShow
ms.assetid: 3b9793e6-e5f4-432f-95f6-62053b955348
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IConfigAviMux interface [DirectShow],SetOutputCompatibilityIndex method, IConfigAviMux.SetOutputCompatibilityIndex, IConfigAviMux::SetOutputCompatibilityIndex, IConfigAviMuxSetOutputCompatibilityIndex, SetOutputCompatibilityIndex, SetOutputCompatibilityIndex method [DirectShow], SetOutputCompatibilityIndex method [DirectShow],IConfigAviMux interface, dshow.iconfigavimux_setoutputcompatibilityindex, strmif/IConfigAviMux::SetOutputCompatibilityIndex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IConfigAviMux.SetOutputCompatibilityIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConfigAviMux::SetOutputCompatibilityIndex


## -description



The <code>SetOutputCompatibilityIndex</code> method sets the AVI index format.




## -parameters




### -param fOldIndex [in]

Specifies one of the following values:

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>Create an AVI 1.0 index, as well as an AVI 2.0 index.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>Create an AVI 2.0 index, but not an AVI 1.0 index.</td>
</tr>
</table>
 


## -returns



Returns S_OK if successful, or an error code otherwise.




## -remarks



The AVI Mux filter always creates an AVI 2.0 index ('indx' format). If the value given in <i>fOldIndex</i> is <b>TRUE</b>, the AVI Mux also creates an AVI 1.0 index ('idx1' format), for backward compatibility with Video for Windows.

The AVI 2.0 index format allows for larger files, incremental growth of files, and minimized disk seeks.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4cc3cdeb-ebc5-46e1-8cc4-84b40e91323b">IConfigAviMux Interface</a>
 

 

