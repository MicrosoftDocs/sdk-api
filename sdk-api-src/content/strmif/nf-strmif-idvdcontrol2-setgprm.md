---
UID: NF:strmif.IDvdControl2.SetGPRM
title: IDvdControl2::SetGPRM
author: windows-sdk-content
description: The SetGPRM method sets a general parameter register value.
old-location: dshow\idvdcontrol2_setgprm.htm
tech.root: DirectShow
ms.assetid: 192bbf1d-a5de-4acf-b8d6-8a5f733da3a6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDvdControl2 interface [DirectShow],SetGPRM method, IDvdControl2.SetGPRM, IDvdControl2::SetGPRM, IDvdControl2SetGPRM, SetGPRM, SetGPRM method [DirectShow], SetGPRM method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_setgprm, strmif/IDvdControl2::SetGPRM
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
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
 - IDvdControl2.SetGPRM
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvdControl2::SetGPRM


## -description



The <code>SetGPRM</code> method sets a general parameter register value.




## -parameters




### -param ulIndex [in]

Register index; may be a value from zero through 15.


### -param wValue [in]

A 16-bit value contained in the specified register.


### -param dwFlags [in]

Bitwise OR of one or more flags from the <a href="https://msdn.microsoft.com/05eb5ab8-a1b3-4876-bac3-29510af8cdbd">DVD_CMD_FLAGS</a> enumeration, specifying how to synchronize the command.


### -param ppCmd [out]

Receives a pointer to an <a href="https://msdn.microsoft.com/85f9b208-ddc2-4d9c-a30b-b666c81a49d2">IDvdCmd</a> object that can be used to synchronize DVD commands. The caller must release the interface. This parameter can be <b>NULL</b>. For more information, see <a href="https://msdn.microsoft.com/37e8f940-617d-43f6-92bd-aadccafe0059">Synchronizing DVD Commands</a>.


## -returns



Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ulIndex</i> parameter is greater than 15 or any other of the input parameters are invalid.

</td>
</tr>
</table>
 




## -remarks



A DVD disc uses general parameter registers to store various types of information. By manually setting one or more of these registers, an application might be able to provide certain custom functionality. This is an advanced command and should not be used unless you have a thorough understanding of the DVD specification.

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>Annex J Command Name
            </td>
<td>Valid Domains
            </td>
</tr>
<tr>
<td>none</td>
<td>All</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2 Interface</a>



<a href="https://msdn.microsoft.com/994f57b5-8514-4768-a679-21133ec92e32">IDvdInfo2::GetAllGPRMs</a>
 

 

