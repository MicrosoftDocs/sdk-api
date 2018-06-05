---
UID: NF:iads.IADsADSystemInfo.GetAnyDCName
title: IADsADSystemInfo::GetAnyDCName
author: windows-sdk-content
description: Retrieves the DNS name of a domain controller in the local computer's domain.
old-location: adsi\iadsadsysteminfo_getanydcname.htm
old-project: ADSI
ms.assetid: 02bc092a-f5ef-4f9d-b9a6-e03aba784d66
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: GetAnyDCName, GetAnyDCName method [ADSI], GetAnyDCName method [ADSI],IADsADSystemInfo interface, IADsADSystemInfo interface [ADSI],GetAnyDCName method, IADsADSystemInfo.GetAnyDCName, IADsADSystemInfo::GetAnyDCName, _ds_iadsadsysteminfo_getanydcname, adsi.iadsadsysteminfo__getanydcname, adsi.iadsadsysteminfo_getanydcname, iads/IADsADSystemInfo::GetAnyDCName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: iads.h
req.include-header: 
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
req.typenames: ADS_SD_FORMAT_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Activeds.dll
api_name:
-	IADsADSystemInfo.GetAnyDCName
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADsADSystemInfo::GetAnyDCName


## -description


The <b>IADsADSystemInfo::GetAnyDCName</b> method retrieves the DNS name of a domain controller in the local computer's domain.


## -parameters




### -param pszDCName [out]

Name of a domain controller, such as "ADServer1.domain1.Fabrikam.com".


## -returns



This method supports the standard <b>HRESULT</b> return values. For more information, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/5573d37b-10a8-4176-80c7-711552ff36cb">IADsADSystemInfo</a>
 

 

