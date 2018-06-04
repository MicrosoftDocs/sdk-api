---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# RoRegisterActivationFactories function


## -description


Registers an array out-of-process activation factories for a Windows Runtime exe server.


## -parameters




### -param activatableClassIds [in]

Type: <b><a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a>*</b>

An array of class identifiers that are associated with activatable runtime classes.


### -param activationFactoryCallbacks [in]

Type: <b><a href="https://msdn.microsoft.com/59660F0E-C2BE-4670-86B7-8C9CBA025910">PFNGETACTIVATIONFACTORY</a>*</b>

An array of callback functions that you can use to retrieve the activation factories that correspond with  <i>activatableClassIds</i>.


### -param count [in]

Type: <b>UINT32</b>

The number of items in the <i>activatableClassIds</i> and <i>activationFactoryCallbacks</i> arrays.


### -param cookie [out]

Type: <b><a href="https://msdn.microsoft.com/D74E5886-45DB-40DE-9740-D14341E78713">RO_REGISTRATION_COOKIE</a>*</b>

A cookie that identifies the registered factories.


## -returns



Type: <b>HRESULT</b>

This function can return one of these values.

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
The  activation factory was registered successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>cookie</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The thread is in a neutral apartment.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_NOTINITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The thread has not been initialized in the Windows Runtime by calling the <a href="https://msdn.microsoft.com/527A7FF7-749D-4178-A397-5C538F6031F8">RoInitialize</a> function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_ALREADYINITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The factory has been initialized already. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
The class is not registered as OutOfProc.

</td>
</tr>
</table>
 




## -remarks



The <b>RoRegisterActivationFactories</b> function enables an exe server to register multiple activation factories without experiencing a race condition.




## -see-also




<a href="https://msdn.microsoft.com/D74E5886-45DB-40DE-9740-D14341E78713">RO_REGISTRATION_COOKIE</a>



<a href="https://msdn.microsoft.com/527A7FF7-749D-4178-A397-5C538F6031F8">RoInitialize</a>
 

 

