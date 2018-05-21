---
UID: NS:difxapi.INSTALLERINFO_W
title: INSTALLERINFO_W
author: windows-driver-content
description: The INSTALLERINFO structure contains information about an application that DIFxAPI associates with a driver package.
old-location: devinst\installerinfo.htm
old-project: devinst
ms.assetid: c8880572-12ac-4be3-b078-4c5d7cc831d4
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*PINSTALLERINFO_W, INSTALLERINFO, INSTALLERINFO structure [Device and Driver Installation], INSTALLERINFO_W, PINSTALLERINFO, PINSTALLERINFO structure pointer [Device and Driver Installation], devinst.installerinfo, difxapi-ref_2dcae2de-7f56-47e6-bbba-5e9527d56311.xml, difxapi/INSTALLERINFO, difxapi/PINSTALLERINFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: difxapi.h
req.include-header: Difxapi.h
req.target-type: Windows
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
req.typenames: INSTALLERINFO_W, *PINSTALLERINFO_W
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	difxapi.h
api_name:
-	INSTALLERINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# INSTALLERINFO_W structure


## -description


The INSTALLERINFO structure contains information about an application that DIFxAPI associates with a <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff544817">driver package</a>. 


## -struct-fields




### -field pApplicationId

A pointer to a NULL-terminated string that supplies a vendor-defined token. DIFxAPI uses this token to associate an application with the <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff544817">driver package</a>. We recommend that the token be a unique application-specific value, such as a <a href="https://msdn.microsoft.com/library/windows/hardware/dn922935">GUID</a>. DIFxAPI does not enforce uniqueness among the tokens. If a caller supplies an INSTALLERINFO structure that specifies an association between an application and a driver package, this member must not be <b>NULL</b> or supply an empty string.


### -field pDisplayName

A pointer to a constant NULL-terminated string that supplies the display name of an application that is associated with a <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff544817">driver package</a>. DIFxAPI requires an application display name to inform a user which application is associated with a driver package. 

For example, for each driver package that is installed by the DIFx tools, an entry, which represents the driver package, is added to <b>Programs and Features</b> in Control Panel. If a user clicks on the <b>Uninstall/Change</b> button of this <b>Programs and Features</b> entry, the resulting dialog box lists the display names of the applications that are associated with the driver package. If a caller supplies an INSTALLERINFO structure that specifies an association between an application and a driver package, this member must not be <b>NULL</b> or supply an empty string.

<div class="alert"><b>Note</b>  In versions of Windows earlier than Windows Vista, the DIFx tools added the entry for the driver package to <b>Add or Remove Programs </b>in Control Panel.</div>
<div> </div>

### -field pProductName

A pointer to a constant NULL-terminated string that supplies the name of the product for an application that is associated with a <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff544817">driver package</a>. If a caller supplies an INSTALLERINFO structure that specifies an association between an application and a driver package, this member must not be <b>NULL</b> or supply an empty string.


### -field pMfgName

A pointer to a constant NULL-terminated string that supplies the name of the manufacturer of the application that is associated with a <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff544817">driver package</a>. If a caller supplies an INSTALLERINFO structure that specifies an association between an application and a driver package, this member must not be <b>NULL</b> or supply an empty string.


## -remarks



The INSTALLERINFO structure is defined specifically as an input parameter to <a href="https://msdn.microsoft.com/library/windows/hardware/ff544813">DriverPackageInstall</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff544822">DriverPackageUninstall</a>. If a caller supplies a non-<b>NULL</b> INSTALLERINFO structure to these functions, all members of the structure must supply non-empty string values; otherwise, these functions return ERROR_INVALID_PARAMETER.

A caller that supplies application information to install a <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff544817">driver package</a> should use the same information to uninstall the driver package. Otherwise, the correct association between applications and the driver package cannot be maintained. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff544813">DriverPackageInstall</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544822">DriverPackageUninstall</a>
 

 

