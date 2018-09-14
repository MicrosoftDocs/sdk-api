---
UID: NF:wmp.IWMPMediaCollection2.createQuery
title: IWMPMediaCollection2::createQuery
author: windows-sdk-content
description: The createQuery method retrieves a pointer to an IWMPQuery interface that represents a new query.
old-location: wmp\iwmpmediacollection2_createquery.htm
tech.root: WMP
ms.assetid: b1e6bf08-3b81-4c04-92ff-73eac5f7495a
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IWMPMediaCollection2 interface [Windows Media Player],createQuery method, IWMPMediaCollection2.createQuery, IWMPMediaCollection2::createQuery, IWMPMediaCollection2createQuery, createQuery, createQuery method [Windows Media Player], createQuery method [Windows Media Player],IWMPMediaCollection2 interface, wmp.iwmpmediacollection2_createquery, wmp/IWMPMediaCollection2::createQuery
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
 - IWMPMediaCollection2.createQuery
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPMediaCollection2::createQuery


## -description



The <b>createQuery</b> method retrieves a pointer to an <b>IWMPQuery</b> interface that represents a new query.




## -parameters




### -param ppQuery [out]

Address of a variable that receives an <b>IWMPQuery</b> pointer to the new, empty query.


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



Creating a new query is the first step toward creating a compound query.

<b>Windows Media Player 10 Mobile:</b> This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/576e231e-542a-495c-ad1b-a246339c3cb1">IWMPMediaCollection2 Interface</a>



<a href="https://msdn.microsoft.com/f1f3c46f-4756-49b4-ad4f-a9097ff787f8">IWMPQuery Interface</a>
 

 

