---
UID: NF:comadmin.ICOMAdminCatalog.GetMultipleComponentsInfo
title: ICOMAdminCatalog::GetMultipleComponentsInfo
author: windows-driver-content
description: Retrieves information about the components found in the specified files.
old-location: cos\icomadmincatalog_getmultiplecomponentsinfo.htm
old-project: cossdk
ms.assetid: dd8c5975-c67a-4f1b-9d48-25053ba5c0e9
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: COMAdminComponentAlreadyInstalled, COMAdminComponentCOMPlusPropertiesFound, COMAdminComponentFlagTypeInfoFound, COMAdminComponentInterfacesFound, COMAdminComponentNotInApplication, COMAdminComponentProxyFound, COMAdminFileFlagAlreadyInstalled, COMAdminFileFlagBadTLB, COMAdminFileFlagCOM, COMAdminFileFlagClassNotAvailable, COMAdminFileFlagContainsComp, COMAdminFileFlagContainsRS, COMAdminFileFlagContainsTLB, COMAdminFileFlagDLLRegsvrFailed, COMAdminFileFlagDoesNotExist, COMAdminFileFlagError, COMAdminFileFlagGetClassObjFailed, COMAdminFileFlagLoadable, COMAdminFileFlagNoRegistrar, COMAdminFileFlagRegTLBFailed, COMAdminFileFlagRegistrar, COMAdminFileFlagRegistrarFailed, COMAdminFileFlagSelfReg, COMAdminFileFlagSelfUnReg, COMAdminFileFlagUnloadableDLL, GetMultipleComponentsInfo, GetMultipleComponentsInfo method [COM+], GetMultipleComponentsInfo method [COM+],ICOMAdminCatalog interface, ICOMAdminCatalog interface [COM+],GetMultipleComponentsInfo method, ICOMAdminCatalog.GetMultipleComponentsInfo, ICOMAdminCatalog::GetMultipleComponentsInfo, _cos_ICOMAdminCatalog_GetMultipleComponentsInfo, comadmin/ICOMAdminCatalog::GetMultipleComponentsInfo, cos.icomadmincatalog_getmultiplecomponentsinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComAdmin.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: COMAdminTxIsolationLevelOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComAdmin.h
api_name:
-	ICOMAdminCatalog.GetMultipleComponentsInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICOMAdminCatalog::GetMultipleComponentsInfo


## -description


Retrieves information about the components found in the specified files.


## -parameters




### -param bstrApplIdOrName [in]

The GUID or application name representing the application.


### -param ppsaVarFileNames [in]

An array of names of files containing the components.


### -param ppsaVarCLSIDs [out]

An array of component CLSIDs.


### -param ppsaVarClassNames [out]

An array of component class names.


### -param ppsaVarFileFlags [out]

An array for file flags containing information about the files.



#### COMAdminFileFlagLoadable
 (0x00000001)



#### COMAdminFileFlagCOM (0x00000002)



#### COMAdminFileFlagContainsRS (0x00000004)



#### COMAdminFileFlagContainsComp (0x00000008)



#### COMAdminFileFlagContainsTLB (0x00000010)



#### COMAdminFileFlagSelfReg (0x00000020)



#### COMAdminFileFlagSelfUnReg (0x00000040)



#### COMAdminFileFlagUnloadableDLL (0x00000080)



#### COMAdminFileFlagDoesNotExist (0x00000100)



#### COMAdminFileFlagAlreadyInstalled (0x00000200)



#### COMAdminFileFlagBadTLB (0x00000400)



#### COMAdminFileFlagGetClassObjFailed (0x00000800)



#### COMAdminFileFlagClassNotAvailable (0x00001000)



#### COMAdminFileFlagRegistrar (0x00002000)



#### COMAdminFileFlagNoRegistrar (0x00004000)



#### COMAdminFileFlagDLLRegsvrFailed (0x00008000)



#### COMAdminFileFlagRegTLBFailed (0x00010000)



#### COMAdminFileFlagRegistrarFailed (0x00020000)



#### COMAdminFileFlagError (0x00040000)


### -param ppsaVarComponentFlags [out]

An array for the component flags used to represent information about components in files.



#### COMAdminComponentFlagTypeInfoFound (0x00000001)



#### COMAdminComponentCOMPlusPropertiesFound (0x00000002)



#### COMAdminComponentProxyFound (0x00000004)



#### COMAdminComponentInterfacesFound (0x00000008)



#### COMAdminComponentAlreadyInstalled (0x00000010)



#### COMAdminComponentNotInApplication (0x00000020)


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and E_FAIL, as well as the following values.

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
<dt><b>COMADMIN_E_OBJECTERRORS</b></dt>
</dl>
</td>
<td width="60%">
Errors occurred while accessing one or more objects.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/2c3c49df-9ca5-40ea-b45c-f4eca1004602">ICOMAdminCatalog</a>
 

 

