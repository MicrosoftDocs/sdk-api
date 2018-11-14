---
UID: NS:oleauto.tagMETHODDATA
title: tagMETHODDATA
author: windows-sdk-content
description: Describes a method or property.
old-location: automat\methoddata.htm
tech.root: automat
ms.assetid: 85fd7121-3eed-4a83-9ba2-caa81fa1e048
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*LPMETHODDATA, DISPATCH_METHOD, DISPATCH_PROPERTYGET, DISPATCH_PROPERTYPUT, DISPATCH_PROPERTYPUTREF, LPMETHODDATA, LPMETHODDATA structure pointer [Automation], METHODDATA, METHODDATA structure [Automation], _oa96_METHODDATA, automat.methoddata, oleauto/LPMETHODDATA, oleauto/METHODDATA, tagMETHODDATA"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: oleauto.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OleAuto.h
api_name:
 - METHODDATA
product: Windows
targetos: Windows
req.typenames: METHODDATA, *LPMETHODDATA
req.redist: 
---

# tagMETHODDATA structure


## -description


Describes a method or property.


## -struct-fields




### -field szName

 The method name.


### -field ppdata

An array of method parameters.


### -field dispid

 The ID of the method, as used in <a href="https://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>.



### -field iMeth

 The index of the method in the VTBL of the interface, starting with 0.



### -field cc

The calling convention. The CDECL and Pascal calling conventions are supported by the dispatch interface creation functions, such as <a href="https://msdn.microsoft.com/45a59243-df93-41ca-ac60-354cb1165004">CreateStdDispatch</a>.



### -field cArgs

 The number of arguments.


### -field wFlags

Invoke flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DISPATCH_METHOD"></a><a id="dispatch_method"></a><dl>
<dt><b>DISPATCH_METHOD</b></dt>
</dl>
</td>
<td width="60%">
The member is invoked as a method. If a property has the same name, both this and the DISPATCH_PROPERTYGET flag can be set.


</td>
</tr>
<tr>
<td width="40%"><a id="DISPATCH_PROPERTYGET"></a><a id="dispatch_propertyget"></a><dl>
<dt><b>DISPATCH_PROPERTYGET</b></dt>
</dl>
</td>
<td width="60%">
The member is retrieved as a property or data member.


</td>
</tr>
<tr>
<td width="40%"><a id="DISPATCH_PROPERTYPUT"></a><a id="dispatch_propertyput"></a><dl>
<dt><b>DISPATCH_PROPERTYPUT</b></dt>
</dl>
</td>
<td width="60%">
The member is set as a property or data member.


</td>
</tr>
<tr>
<td width="40%"><a id="DISPATCH_PROPERTYPUTREF"></a><a id="dispatch_propertyputref"></a><dl>
<dt><b>DISPATCH_PROPERTYPUTREF</b></dt>
</dl>
</td>
<td width="60%">
The member is changed by a reference assignment, rather than a value assignment. This flag is valid only when the property accepts a reference to an object.


</td>
</tr>
</table>
 


### -field vtReturn

The return type for the method.

