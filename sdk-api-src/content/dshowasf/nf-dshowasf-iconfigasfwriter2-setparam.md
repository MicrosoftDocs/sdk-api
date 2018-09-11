---
UID: NF:dshowasf.IConfigAsfWriter2.SetParam
title: IConfigAsfWriter2::SetParam
author: windows-sdk-content
description: The SetParam method sets the value of the specified filter configuration parameter.
old-location: dshow\iconfigasfwriter2_setparam.htm
tech.root: DirectShow
ms.assetid: 0294837c-0cf2-4a05-bef4-16d13864f759
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IConfigAsfWriter2 interface [DirectShow],SetParam method, IConfigAsfWriter2.SetParam, IConfigAsfWriter2::SetParam, IConfigAsfWriter2SetParam, SetParam, SetParam method [DirectShow], SetParam method [DirectShow],IConfigAsfWriter2 interface, dshow.iconfigasfwriter2_setparam, dshowasf/IConfigAsfWriter2::SetParam
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dshowasf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - Dshowasf.h
api_name:
 - IConfigAsfWriter2.SetParam
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConfigAsfWriter2::SetParam


## -description



The <code>SetParam</code> method sets the value of the specified filter configuration parameter.




## -parameters




### -param dwParam [in]

Specifies the parameter to set,as a member of the <a href="https://msdn.microsoft.com/aa274c86-f75d-40ee-8c46-918ccffdfd03">_AM_ASFWRITERCONFIG_PARAM</a> enumeration.


### -param dwParam1 [in]

Specifies the value to assign to the <i>dwParam</i> parameter.


### -param dwParam2 [out]

Reserved. Must be zero.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/dffda43a-5831-4889-864f-81351b9e2bb3">Creating ASF Files in DirectShow</a>



<a href="https://msdn.microsoft.com/fd931a95-3678-46de-8f17-9e7c27087398">IConfigAsfWriter2 Interface</a>
 

 

