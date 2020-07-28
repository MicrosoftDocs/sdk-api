---
UID: NF:comadmin.ICOMAdminCatalog2.ImportComponents
title: ICOMAdminCatalog2::ImportComponents (comadmin.h)
description: Imports the specified components that are already registered into an application.
helpviewer_keywords: ["COMAdmin32BitComponent","COMAdmin64BitComponent","ICOMAdminCatalog2 interface [COM+]","ImportComponents method","ICOMAdminCatalog2.ImportComponents","ICOMAdminCatalog2::ImportComponents","ImportComponents","ImportComponents method [COM+]","ImportComponents method [COM+]","ICOMAdminCatalog2 interface","_cos_icomadmincatalog2_ImportComponents","comadmin/ICOMAdminCatalog2::ImportComponents","cos.icomadmincatalog2_importcomponents"]
old-location: cos\icomadmincatalog2_importcomponents.htm
tech.root: cos
ms.assetid: a7ae28f9-6be6-4774-974a-a5d7f3ebbc02
ms.date: 12/05/2018
ms.keywords: COMAdmin32BitComponent, COMAdmin64BitComponent, ICOMAdminCatalog2 interface [COM+],ImportComponents method, ICOMAdminCatalog2.ImportComponents, ICOMAdminCatalog2::ImportComponents, ImportComponents, ImportComponents method [COM+], ImportComponents method [COM+],ICOMAdminCatalog2 interface, _cos_icomadmincatalog2_ImportComponents, comadmin/ICOMAdminCatalog2::ImportComponents, cos.icomadmincatalog2_importcomponents
f1_keywords:
- comadmin/ICOMAdminCatalog2.ImportComponents
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICOMAdminCatalog2::ImportComponents


## -description


Imports the specified components that are already registered into an application.

To import unconfigured components, you can use the <a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-importunconfiguredcomponents">ImportUnconfiguredComponents</a> and <a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-promoteunconfiguredcomponents">PromoteUnconfiguredComponents</a> methods.


## -parameters




### -param bstrApplicationIDOrName [in]

The application ID or name of the application into which the components are to be imported.


### -param pVarCLSIDOrProgID [in]

The components to be imported. Each element of the <b>Variant</b> may be a <b>String</b> containing a class ID or program ID, a single catalog object, or a catalog collection (for example, as returned by the <a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-getcollectionbyquery2">GetCollectionByQuery2</a> method).


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




<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nn-comadmin-icomadmincatalog2">ICOMAdminCatalog2</a>
 

 

