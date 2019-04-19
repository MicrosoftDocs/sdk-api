---
UID: NF:wmp.IWMPLibrary.get_name
title: IWMPLibrary::get_name (wmp.h)
author: windows-sdk-content
description: The get_name method retrieves the display name of the current library.
old-location: wmp\iwmplibrary_get_name.htm
tech.root: WMP
ms.assetid: 28f1e3bc-3692-4fd0-a0b3-fecc3a173103
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPLibrary interface [Windows Media Player],get_name method, IWMPLibrary.get_name, IWMPLibrary::get_name, IWMPLibraryget_name, get_name, get_name method [Windows Media Player], get_name method [Windows Media Player],IWMPLibrary interface, wmp.iwmplibrary_get_name, wmp/IWMPLibrary::get_name
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
 - IWMPLibrary.get_name
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPLibrary::get_name


## -description



The <b>get_name</b> method retrieves the display name of the current library.




## -parameters




### -param pbstrName [out]

Pointer to a string containing the name of the current library.


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




<a href="https://msdn.microsoft.com/en-us/library/Dd563383(v=VS.85).aspx">IWMPLibrary Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563394(v=VS.85).aspx">IWMPLibrary::get_type</a>
 

 

