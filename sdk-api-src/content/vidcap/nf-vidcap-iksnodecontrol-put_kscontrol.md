---
UID: NF:vidcap.IKsNodeControl.put_KsControl
title: IKsNodeControl::put_KsControl
author: windows-sdk-content
description: Provides an instance of the IKsControl interface to the extension unit.
old-location: dshow\iksnodecontrol_put_kscontrol.htm
tech.root: DirectShow
ms.assetid: 145967fc-3124-4e3b-b1ce-a381ea97cb89
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IKsNodeControl interface [DirectShow],put_KsControl method, IKsNodeControl.put_KsControl, IKsNodeControl::put_KsControl, IKsNodeControlput_KsControl, dshow.iksnodecontrol_put_kscontrol, put_KsControl, put_KsControl method [DirectShow], put_KsControl method [DirectShow],IKsNodeControl interface, vidcap/IKsNodeControl::put_KsControl
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vidcap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
 - Vidcap.h
api_name:
 - IKsNodeControl.put_KsControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IKsNodeControl::put_KsControl


## -description



Provides an instance of the <b>IKsControl</b> interface to the extension unit.




## -parameters




### -param pKsControl [in]

Pointer to the <b>IKsControl</b> interface, typed as a void pointer.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



The KsProxy filter calls this method with a pointer to its own <b>IKsControl</b> interface. The extension unit should cache the pointer.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/c38ce847-726a-4c1a-9276-810385af6c9f">IKsNodeControl Interface</a>
 

 

