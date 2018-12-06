---
UID: NF:xpsobjectmodel.IXpsOMPackage.SetCoreProperties
title: IXpsOMPackage::SetCoreProperties
author: windows-sdk-content
description: Sets the IXpsOMCoreProperties interface of the XPS package.
old-location: xps\ixpsompackage_setcoreproperties.htm
tech.root: printdocs
ms.assetid: e1be5c48-1e2b-4f94-98ec-b61bc255e63b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IXpsOMPackage interface [XPS Documents and Packaging],SetCoreProperties method, IXpsOMPackage.SetCoreProperties, IXpsOMPackage::SetCoreProperties, SetCoreProperties, SetCoreProperties method [XPS Documents and Packaging], SetCoreProperties method [XPS Documents and Packaging],IXpsOMPackage interface, xps.ixpsompackage_setcoreproperties, xpsobjectmodel/IXpsOMPackage::SetCoreProperties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMPackage.SetCoreProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMPackage::SetCoreProperties


## -description


Sets the <a href="https://msdn.microsoft.com/705ec9c7-5aa9-4fc5-ad2c-441cb545d056">IXpsOMCoreProperties</a> interface of the XPS package.


## -parameters




### -param coreProperties [in]

The <a href="https://msdn.microsoft.com/705ec9c7-5aa9-4fc5-ad2c-441cb545d056">IXpsOMCoreProperties</a> interface pointer to be assigned to the package.
          A <b>NULL</b> pointer releases any previously assigned core properties interface.


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
<dt><b>XPS_E_NO_CUSTOM_OBJECTS</b></dt>
</dl>
</td>
<td width="60%">
<i>coreProperties</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/705ec9c7-5aa9-4fc5-ad2c-441cb545d056">IXpsOMCoreProperties</a>



<a href="https://msdn.microsoft.com/7b0a36d6-1af1-4c2c-af14-d6139e9115c3">IXpsOMPackage</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

