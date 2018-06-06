---
UID: NF:wmp.IWMPCore.get_cdromCollection
title: IWMPCore::get_cdromCollection
author: windows-sdk-content
description: The get_cdromCollection method retrieves a pointer to an IWMPCdromCollection interface.
old-location: wmp\iwmpcore_get_cdromcollection.htm
old-project: WMP
ms.assetid: 6bb6500e-7a30-400b-a88b-7ee3596501b1
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPCore interface [Windows Media Player],get_cdromCollection method, IWMPCore.get_cdromCollection, IWMPCore::get_cdromCollection, IWMPCoreget_cdromCollection, get_cdromCollection, get_cdromCollection method [Windows Media Player], get_cdromCollection method [Windows Media Player],IWMPCore interface, wmp.iwmpcore_get_cdromcollection, wmp/IWMPCore::get_cdromCollection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
tech.root: 
req.typenames: WMPSyncState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPCore.get_cdromCollection
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPCore::get_cdromCollection


## -description



The <b>get_cdromCollection</b> method retrieves a pointer to an <b>IWMPCdromCollection</b> interface.




## -parameters




### -param ppCdromCollection [out]

Pointer to a pointer to an <b>IWMPCdromCollection</b> interface.


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



Before calling this method, you must have read access to the library. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.




## -see-also




<a href="https://msdn.microsoft.com/ba55ac32-149d-4f7b-a2bb-1fdb0be806cd">IWMPCdromCollection Interface</a>



<a href="https://msdn.microsoft.com/24fbb34d-4a5e-4a00-85fc-9659a31dc650">IWMPCore Interface</a>
 

 

