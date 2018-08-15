---
UID: NF:gpedit.IGPEInformation.GetDSPath
title: IGPEInformation::GetDSPath
author: windows-sdk-content
description: The GetDSPath method retrieves the Active Directory path for the specified section of the GPO.
old-location: policy\igpeinformation_getdspath.htm
old-project: Policy
ms.assetid: 0cf969b2-40a9-4fbd-ba2b-38979fb5796a
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GPO_SECTION_MACHINE, GPO_SECTION_ROOT, GPO_SECTION_USER, GetDSPath, GetDSPath method [Group Policy], GetDSPath method [Group Policy],IGPEInformation interface, IGPEInformation interface [Group Policy],GetDSPath method, IGPEInformation.GetDSPath, IGPEInformation::GetDSPath, _win32_igpeinformation_getdspath, gpedit/IGPEInformation::GetDSPath, policy.igpeinformation_getdspath
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gpedit.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpedit.dll
api_name:
 - IGPEInformation.GetDSPath
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpedit.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPEInformation::GetDSPath


## -description


The
    <b>GetDSPath</b> method retrieves the Active Directory path for the specified section of the GPO.


## -parameters




### -param dwSection [in]

Specifies the GPO section. This parameter can be one of the following values.



#### GPO_SECTION_ROOT

Root section



#### GPO_SECTION_USER

User section



#### GPO_SECTION_MACHINE

Computer section


### -param pszPath [out]

Receives the Active Directory path to the root of the requested section. For more information, see the following Remarks section.


### -param cchMaxPath [in]

Specifies the size, in characters, of the <i>pszPath</i> parameter.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.




## -remarks



If you call the 
<b>GetDSPath</b> method and specify a computer GPO, the method succeeds, but on return, the <i>pszPath</i> parameter contains an empty string. This is because computer GPOs do not have Active Directory storage; they have only file system storage.

To retrieve the file system path for the specified section of a GPO, you can call the 
<a href="https://msdn.microsoft.com/6fcdc7f8-61bf-4d3e-b0aa-ff730d6730cb">GetFileSysPath</a> method.




## -see-also




<a href="https://msdn.microsoft.com/6fcdc7f8-61bf-4d3e-b0aa-ff730d6730cb">GetFileSysPath</a>



<a href="https://msdn.microsoft.com/dc15a69d-a44d-4731-a9e5-6165abd581c4">Group Policy
    Interfaces</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/3b3e7793-fc69-43a3-a2b1-0aa36748a19b">IGPEInformation</a>
 

 

