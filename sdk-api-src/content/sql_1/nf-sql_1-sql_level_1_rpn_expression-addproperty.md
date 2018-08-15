---
UID: NF:sql_1.SQL_LEVEL_1_RPN_EXPRESSION.AddProperty
title: AddProperty function
author: windows-sdk-content
description: The AddProperty function adds one property to the parser property database.
old-location: netmon\addproperty.htm
old-project: NetMon2
ms.assetid: 7aa9af0a-2434-4331-a244-a743dd430dcf
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AddProperty, AddProperty function [Network Monitor], _netmon_addproperty, netmon.addproperty, sql_1/AddProperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: sql_1.h
req.include-header: Netmon.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: WORDLIST_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Nmapi.dll
api_name:
 - AddProperty
product: Windows
targetos: Windows
req.lib: Nmapi.lib
req.dll: Nmapi.dll
req.irql: 
req.product: Outlook Express 6.0
---

# AddProperty function


## -description


The <b>AddProperty</b> function adds one property to the parser <a href="https://msdn.microsoft.com/en-us/library/Ee832004(v=VS.85).aspx">property database</a>.


## -parameters




### -param pProp [in]

Handle of the protocol that is associated with the database. When Network Monitor calls the 
<a href="https://msdn.microsoft.com/b8a2752d-30a6-48f2-90b3-b1430ae983d2">Register</a> function, Network Monitor passes the protocol handle to the parser DLL.


#### - PropertyInfo [in]

Pointer to a 
<a href="https://msdn.microsoft.com/878777ab-141d-4cc5-b0c1-f2ac8f770bf0">PROPERTYINFO</a> structure that defines the property.


## -returns



If the function is successful, the return value is a pointer to the property that is added.

If the function is unsuccessful, the return value is <b>NULL</b>.




## -remarks



The <b>AddProperty</b> function should be called only when implementing the 
<a href="https://msdn.microsoft.com/b8a2752d-30a6-48f2-90b3-b1430ae983d2">Register</a> function. The parser uses <b>AddProperty</b> to add a property to the <a href="https://msdn.microsoft.com/en-us/library/Ee832004(v=VS.85).aspx">property database</a> of the protocol. Properties are added to the database one property at a time.

<b>AddProperty</b> must be called after calling 
<a href="https://msdn.microsoft.com/0a3be6ae-d7ce-4315-b4f2-b46bcfa25b69">CreatePropertyDatabase</a>. If <b>AddProperty</b> is called before the property database is created, Network Monitor returns the NMERR_NO_PROPERTY_DATABASE error.




## -see-also




<a href="https://msdn.microsoft.com/0a3be6ae-d7ce-4315-b4f2-b46bcfa25b69">CreatePropertyDatabase</a>



<a href="https://msdn.microsoft.com/878777ab-141d-4cc5-b0c1-f2ac8f770bf0">PROPERTYINFO</a>



<a href="https://msdn.microsoft.com/b8a2752d-30a6-48f2-90b3-b1430ae983d2">Register</a>
 

 

