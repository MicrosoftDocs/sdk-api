---
UID: NF:mbnapi.IMbnConnectionProfile.GetProfileXmlData
title: IMbnConnectionProfile::GetProfileXmlData
author: windows-sdk-content
description: Gets the XML data of the current profile.
old-location: mbn\imbnconnectionprofile_getprofilexmldata.htm
old-project: mbn
ms.assetid: 4a94dd33-1dad-4d0a-98e8-1ccce83f345e
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetProfileXmlData, GetProfileXmlData method [Microsoft Broadband Networks], GetProfileXmlData method [Microsoft Broadband Networks],IMbnConnectionProfile interface, IMbnConnectionProfile interface [Microsoft Broadband Networks],GetProfileXmlData method, IMbnConnectionProfile.GetProfileXmlData, IMbnConnectionProfile::GetProfileXmlData, mbn.imbnconnectionprofile_getprofilexmldata, mbnapi/IMbnConnectionProfile::GetProfileXmlData
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MBN_VOICE_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnConnectionProfile.GetProfileXmlData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnConnectionProfile::GetProfileXmlData


## -description


Gets the XML data of the current profile.


## -parameters




### -param profileData [out, retval]

A pointer to a string containing the profile in XML format.  If the method returns S_OK, the calling application must free the allocated memory by calling <a href=" http://go.microsoft.com/fwlink/p/?linkid=120718">SysFreeString</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The data provided by this method complies with the <a href="https://msdn.microsoft.com/bfec0a1d-de17-4ebd-b9fb-570e230da317">Mobile Broadband Profile Schema Reference</a>.  The data will not contain the password used in the profile. 




## -see-also




<a href="https://msdn.microsoft.com/f7730efe-e367-4642-8482-2a23052bab0c">IMbnConnectionProfile</a>
 

 

