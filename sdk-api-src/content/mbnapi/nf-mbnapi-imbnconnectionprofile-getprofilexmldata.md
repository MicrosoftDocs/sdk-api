---
UID: NF:mbnapi.IMbnConnectionProfile.GetProfileXmlData
title: IMbnConnectionProfile::GetProfileXmlData (mbnapi.h)
description: Gets the XML data of the current profile.
old-location: mbn\imbnconnectionprofile_getprofilexmldata.htm
tech.root: mbn
ms.assetid: 4a94dd33-1dad-4d0a-98e8-1ccce83f345e
ms.date: 12/05/2018
ms.keywords: GetProfileXmlData, GetProfileXmlData method [Microsoft Broadband Networks], GetProfileXmlData method [Microsoft Broadband Networks],IMbnConnectionProfile interface, IMbnConnectionProfile interface [Microsoft Broadband Networks],GetProfileXmlData method, IMbnConnectionProfile.GetProfileXmlData, IMbnConnectionProfile::GetProfileXmlData, mbn.imbnconnectionprofile_getprofilexmldata, mbnapi/IMbnConnectionProfile::GetProfileXmlData
ms.topic: method
f1_keywords:
- mbnapi/IMbnConnectionProfile.GetProfileXmlData
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mbnapi.h
api_name:
- IMbnConnectionProfile.GetProfileXmlData
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnConnectionProfile::GetProfileXmlData


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Gets the XML data of the current profile.


## -parameters




### -param profileData [out, retval]

A pointer to a string containing the profile in XML format.  If the method returns S_OK, the calling application must free the allocated memory by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=120718">SysFreeString</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The data provided by this method complies with the <a href="https://docs.microsoft.com/windows/desktop/mbn/schema-schema">Mobile Broadband Profile Schema Reference</a>.  The data will not contain the password used in the profile. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile">IMbnConnectionProfile</a>
 

 

