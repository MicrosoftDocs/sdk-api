---
UID: NF:comadmin.ICOMAdminCatalog2.ImportComponents
title: ICOMAdminCatalog2::ImportComponents
author: windows-sdk-content
description: Imports the specified components that are already registered into an application.
old-location: cos\icomadmincatalog2_importcomponents.htm
tech.root: cossdk
ms.assetid: a7ae28f9-6be6-4774-974a-a5d7f3ebbc02
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: COMAdmin32BitComponent, COMAdmin64BitComponent, ICOMAdminCatalog2 interface [COM+],ImportComponents method, ICOMAdminCatalog2.ImportComponents, ICOMAdminCatalog2::ImportComponents, ImportComponents, ImportComponents method [COM+], ImportComponents method [COM+],ICOMAdminCatalog2 interface, _cos_icomadmincatalog2_ImportComponents, comadmin/ICOMAdminCatalog2::ImportComponents, cos.icomadmincatalog2_importcomponents
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComAdmin.Idl
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
 - ComAdmin.h
api_name:
 - ICOMAdminCatalog2.ImportComponents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- comadmin.h
: 
- ICOMAdminCatalog2.ImportComponents
: 
---

# ICOMAdminCatalog2::ImportComponents


## -description


Imports the specified components that are already registered into an application.

To import unconfigured components, you can use the <a href="https://msdn.microsoft.com/en-us/library/ms681295(v=VS.85).aspx">ImportUnconfiguredComponents</a> and <a href="https://msdn.microsoft.com/en-us/library/ms687606(v=VS.85).aspx">PromoteUnconfiguredComponents</a> methods.


## -parameters




### -param bstrApplicationIDOrName [in]

The application ID or name of the application into which the components are to be imported.


### -param pVarCLSIDOrProgID [in]

The components to be imported. Each element of the <b>Variant</b> may be a <b>String</b> containing a class ID or program ID, a single catalog object, or a catalog collection (for example, as returned by the <a href="https://msdn.microsoft.com/en-us/library/ms685970(v=VS.85).aspx">GetCollectionByQuery2</a> method).


### -param pVarComponentType [in, optional]

The bitnes of each component. This parameter can be one of the following values. If this parameter is omitted, the native bitness of the computer is assumed.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="COMAdmin32BitComponent"></a><a id="comadmin32bitcomponent"></a><a id="COMADMIN32BITCOMPONENT"></a><dl>
<dt><b>COMAdmin32BitComponent</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Uses a 32-bit format.

</td>
</tr>
<tr>
<td width="40%"><a id="COMAdmin64BitComponent"></a><a id="comadmin64bitcomponent"></a><a id="COMADMIN64BITCOMPONENT"></a><dl>
<dt><b>COMAdmin64BitComponent</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
Uses a 64-bit format.

</td>
</tr>
</table>
 


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ee309562(v=VS.85).aspx">ICOMAdminCatalog2</a>
 

 

