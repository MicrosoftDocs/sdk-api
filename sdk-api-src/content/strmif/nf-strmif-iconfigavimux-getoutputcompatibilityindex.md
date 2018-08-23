---
UID: NF:strmif.IConfigAviMux.GetOutputCompatibilityIndex
title: IConfigAviMux::GetOutputCompatibilityIndex
author: windows-sdk-content
description: The GetOutputCompatibilityIndex method retrieves the setting for the AVI index format.
old-location: dshow\iconfigavimux_getoutputcompatibilityindex.htm
old-project: DirectShow
ms.assetid: 723f1662-4f1a-408b-a737-9095e7c14c4f
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: GetOutputCompatibilityIndex, GetOutputCompatibilityIndex method [DirectShow], GetOutputCompatibilityIndex method [DirectShow],IConfigAviMux interface, IConfigAviMux interface [DirectShow],GetOutputCompatibilityIndex method, IConfigAviMux.GetOutputCompatibilityIndex, IConfigAviMux::GetOutputCompatibilityIndex, IConfigAviMuxGetOutputCompatibilityIndex, dshow.iconfigavimux_getoutputcompatibilityindex, strmif/IConfigAviMux::GetOutputCompatibilityIndex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.redist: 
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IConfigAviMux.GetOutputCompatibilityIndex
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IConfigAviMux::GetOutputCompatibilityIndex


## -description



The <code>GetOutputCompatibilityIndex</code> method retrieves the setting for the AVI index format.




## -parameters




### -param pfOldIndex [out]

Receives one of the following values.

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



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -remarks



The AVI Mux filter always creates an AVI 2.0 index ('indx' format). If the value returned in <i>pfOldIndex</i> is <b>TRUE</b>, the AVI Mux also creates an AVI 1.0 index ('idx1' format), for backward compatibility with Video for Windows.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4cc3cdeb-ebc5-46e1-8cc4-84b40e91323b">IConfigAviMux Interface</a>



<a href="https://msdn.microsoft.com/3b9793e6-e5f4-432f-95f6-62053b955348">IConfigAviMux::SetOutputCompatibilityIndex</a>
 

 

