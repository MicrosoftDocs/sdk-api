---
UID: NF:xpsobjectmodel.IXpsOMShareable.GetType
title: IXpsOMShareable::GetType
author: windows-driver-content
description: Gets the object type of the interface.
old-location: xps\ixpsomshareable_gettype.htm
old-project: printdocs
ms.assetid: 1d30e11e-1306-4721-b5fc-0419715ba2c8
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetType, GetType method [XPS Documents and Packaging], GetType method [XPS Documents and Packaging],IXpsOMShareable interface, IXpsOMShareable interface [XPS Documents and Packaging],GetType method, IXpsOMShareable.GetType, IXpsOMShareable::GetType, xps.ixpsomshareable_gettype, xpsobjectmodel/IXpsOMShareable::GetType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: XPS_INTERLEAVING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xpsobjectmodel.h
api_name:
-	IXpsOMShareable.GetType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMShareable::GetType


## -description


Gets the object type of the interface.


## -parameters




### -param type [out, retval]

The <a href="https://msdn.microsoft.com/2e53f22e-7521-45c9-ac88-b76fb381f556">XPS_OBJECT_TYPE</a> value that describes the interface that is derived from <a href="https://msdn.microsoft.com/2071292f-b898-4ec8-99f7-294c8d820965">IXpsOMShareable</a>.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>type</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/2071292f-b898-4ec8-99f7-294c8d820965">IXpsOMShareable</a>
 

 

