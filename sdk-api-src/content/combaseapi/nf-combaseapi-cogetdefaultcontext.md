---
UID: NF:combaseapi.CoGetDefaultContext
title: CoGetDefaultContext function
author: windows-sdk-content
description: Retrieves a reference to the default context of the specified apartment.
old-location: cos\cogetdefaultcontext.htm
tech.root: cossdk
ms.assetid: 97a0e7da-e8bb-4bde-a8ba-35c90a1351d2
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: APTTYPE_CURRENT, APTTYPE_MAINSTA, APTTYPE_MTA, APTTYPE_NA, CoGetDefaultContext, CoGetDefaultContext function [COM+], combaseapi/CoGetDefaultContext, cos.cogetdefaultcontext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: combaseapi.h
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoGetDefaultContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CoGetDefaultContext
: 
---

# CoGetDefaultContext function


## -description


Retrieves a reference to the default context of the specified apartment.


## -parameters




### -param aptType [in]

The apartment type of the default context that is being requested. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="APTTYPE_CURRENT"></a><a id="apttype_current"></a><dl>
<dt><b>APTTYPE_CURRENT</b></dt>
<dt>-1</dt>
</dl>
</td>
<td width="60%">
The caller's apartment.

</td>
</tr>
<tr>
<td width="40%"><a id="APTTYPE_MTA"></a><a id="apttype_mta"></a><dl>
<dt><b>APTTYPE_MTA</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The multithreaded apartment for the current process.

</td>
</tr>
<tr>
<td width="40%"><a id="APTTYPE_NA"></a><a id="apttype_na"></a><dl>
<dt><b>APTTYPE_NA</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The neutral apartment for the current process.

</td>
</tr>
<tr>
<td width="40%"><a id="APTTYPE_MAINSTA"></a><a id="apttype_mainsta"></a><dl>
<dt><b>APTTYPE_MAINSTA</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The main single-threaded apartment for the current process.

</td>
</tr>
</table>
 

The <a href="https://msdn.microsoft.com/en-us/library/ms693793(v=VS.85).aspx">APTTYPE</a> value APTTYPE_STA (0) is not supported. A process can contain multiple single-threaded apartments, each with its own context, so <b>CoGetDefaultContext</b> could not determine which STA is of interest. Therefore, this function returns E_INVALIDARG if APTTYPE_STA is specified.


### -param riid [in]

The interface identifier (IID) of the interface that is being requested on the default context. Typically, the caller requests IID_IObjectContext. The default context does not support all of the normal object context interfaces.


### -param ppv [out]

A reference to the interface specified by riid on the default context. If the object's component is non-configured, (that is, the object's component has not been imported into a COM+ application), or if the <b>CoGetDefaultContext</b> function is called from a constructor or an <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> method, this parameter is set to a <b>NULL</b> pointer.


## -returns



This method can return the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_NOTINITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The caller is not in an initialized apartment.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The object context does not support the interface specified by <i>riid</i>.

</td>
</tr>
</table>
 




## -remarks



Every COM apartment has a special context called the default context. A default context is different from all the other, non-default contexts in an apartment because it does not provide runtime services. It does not support all of the normal object context interfaces.

The default context is also used by instances of non-configured COM components, (that is, components that have not been part of a COM+ application), when they are created from an apartment that does not support their threading model. In other words, if a COM object creates an instance of a non-configured component and the new object cannot be added to its creator's context because of its threading model, the new object is instead added to the default context of an apartment that supports its threading model.

An object should never pass an <a href="https://msdn.microsoft.com/en-us/library/ms684253(v=VS.85).aspx">IObjectContext</a> reference to another object. If you pass an <b>IObjectContext</b> reference to another object, it is no longer a valid reference.

When an object obtains a reference to an <a href="https://msdn.microsoft.com/en-us/library/ms684253(v=VS.85).aspx">IObjectContext</a>, it must release the <b>IObjectContext</b> object when it is finished with it.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms681289(v=VS.85).aspx">COM+ Contexts and Threading Models</a>
 

 

