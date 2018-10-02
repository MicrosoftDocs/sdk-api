---
UID: NF:wmp.IWMPLibrary.get_type
title: IWMPLibrary::get_type
author: windows-sdk-content
description: The get_type method retrieves a value that indicates the library type.
old-location: wmp\iwmplibrary_get_type.htm
tech.root: WMP
ms.assetid: 95f36972-2227-4fe8-88d7-41f7aebbf67a
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMPLibrary interface [Windows Media Player],get_type method, IWMPLibrary.get_type, IWMPLibrary::get_type, IWMPLibraryget_type, get_type, get_type method [Windows Media Player], get_type method [Windows Media Player],IWMPLibrary interface, wmp.iwmplibrary_get_type, wmp/IWMPLibrary::get_type
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wmp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPLibrary.get_type
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPLibrary::get_type


## -description



The <b>get_type</b> method retrieves a value that indicates the library type.




## -parameters




### -param pwmplt [out]

Pointer to a variable that receives a value from the <b>WMPLibraryType</b> enumeration that indicates the library type.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/add0ed43-d83f-4793-b1f6-ccad0f01854c">IWMPLibrary Interface</a>



<a href="https://msdn.microsoft.com/28f1e3bc-3692-4fd0-a0b3-fecc3a173103">IWMPLibrary::get_name</a>



<a href="https://msdn.microsoft.com/bf0e7140-5a33-4841-bd55-ac07dae09c41">WMPLibraryType</a>
 

 

