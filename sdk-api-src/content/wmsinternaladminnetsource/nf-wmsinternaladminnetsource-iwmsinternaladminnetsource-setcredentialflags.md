---
UID: NF:wmsinternaladminnetsource.IWMSInternalAdminNetSource.SetCredentialFlags
title: IWMSInternalAdminNetSource::SetCredentialFlags
author: windows-sdk-content
description: The SetCredentialFlags method is used to set the user preference for automatic password caching.
old-location: wmformat\iwmsinternaladminnetsource_setcredentialflags.htm
old-project: wmformat
ms.assetid: af6208b3-84f6-44d1-9587-140044f2b2f0
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IWMSInternalAdminNetSource interface [windows Media Format],SetCredentialFlags method, IWMSInternalAdminNetSource.SetCredentialFlags, IWMSInternalAdminNetSource::SetCredentialFlags, IWMSInternalAdminNetSourceSetCredentialFlags, SetCredentialFlags, SetCredentialFlags method [windows Media Format], SetCredentialFlags method [windows Media Format],IWMSInternalAdminNetSource interface, wmformat.iwmsinternaladminnetsource_setcredentialflags, wmsinternaladminnetsource/IWMSInternalAdminNetSource::SetCredentialFlags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmsinternaladminnetsource.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
req.typenames: NETSOURCE_URLCREDPOLICY_SETTINGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMSInternalAdminNetSource.SetCredentialFlags
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMSInternalAdminNetSource::SetCredentialFlags


## -description



The <b>SetCredentialFlags</b> method is used to set the user preference for automatic password caching. When your application prompts the user for a password, you can include a checkbox on the dialog box that the user can select to always have passwords saved. You can then set a flag to maintain that preference.




## -parameters




### -param dwFlags [in]

<b>DWORD</b> containing the credential flags. At this time, the only supported flag is 0x1, which signifies that the user has stated a preference that passwords should be saved automatically.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0fbdad85-d94a-4598-bb25-f733df33692a">IWMSInternalAdminNetSource Interface</a>



<a href="https://msdn.microsoft.com/781b2868-c8e2-4d92-98f2-c2950fac3d9b">IWMSInternalAdminNetSource::GetCredentialFlags</a>



<a href="https://msdn.microsoft.com/c0655ed3-8d14-447a-b74f-054498eb75e9">IWMSInternalAdminNetSource::SetCredentials</a>
 

 

