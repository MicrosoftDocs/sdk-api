---
UID: NF:mmc.IComponent2.GetResultViewType2
title: IComponent2::GetResultViewType2
author: windows-sdk-content
description: The GetResultViewType2 method retrieves the result view type. This method supersedes the IComponent::GetResultViewType method.
old-location: mmc\icomponent2_getresultviewtype2.htm
tech.root: MMC
ms.assetid: 687ddb0a-6e10-4553-9885-fd85bf8dd6ff
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetResultViewType2, GetResultViewType2 method [MMC], GetResultViewType2 method [MMC],IComponent2 interface, IComponent2 interface [MMC],GetResultViewType2 method, IComponent2.GetResultViewType2, IComponent2::GetResultViewType2, _slate_icomponent2_getresultviewtype2, mmc.icomponent2_getresultviewtype2, mmc/IComponent2::GetResultViewType2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mmc.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - IComponent2.GetResultViewType2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComponent2::GetResultViewType2


## -description


The 
<b>GetResultViewType2</b> method retrieves the result view type. This method supersedes the 
<a href="https://msdn.microsoft.com/d2575f79-d646-41b5-84a5-768402cfb826">IComponent::GetResultViewType</a> method.


## -parameters




### -param cookie [in]

A value that specifies the snapin-provided unique identifier for the scope item. For more details about cookies in MMC, see <a href="https://msdn.microsoft.com/3b48fb0b-d2c7-41e6-a5bf-277e6f92488b">Cookies</a>.


### -param pResultViewType [in, out]

A pointer to the 
<a href="https://msdn.microsoft.com/50357902-6999-4d65-8e12-81277b66d5ee">RESULT_VIEW_TYPE_INFO</a> structure for the result view. If your snap-in implements 
<a href="https://msdn.microsoft.com/b9e67a37-c09d-46f3-896f-e75122256812">IComponent2</a>, the <b>pstrPersistableViewDescription</b> member of the <b>RESULT_VIEW_TYPE_INFO</b> structure must contain a valid view description string; otherwise, MMC will not initialize your snap-in. The <b>pstrPersistableViewDescription</b> member must be allocated by 
<a href="_com_cotaskmemalloc">CoTaskMemAlloc</a>. The snap-in must not free <b>pstrPersistableViewDescription</b>, as it will be freed by MMC.


## -returns



If successful, the return value is S_OK. Other return values indicate an error code.




## -remarks



During result view creation, MMC calls the snap-in's <b>IComponent2::GetResultViewType2</b> method. When the user revisits the result view named by the <b>pstrPersistableViewDescription</b> member of *<i>pResultViewType</i>, MMC will call the snap-in's 
<a href="https://msdn.microsoft.com/fe9a71c7-eaa6-4479-8337-0746a784a57f">IComponent2::RestoreResultView</a> method, at which time the snap-in can provide snap-in-specific details (if any) for the restored result view. The user revisits the result view by means of the MMC <b>Back/Forward</b> buttons or the loading of a saved console file. For more information about the use of the <b>IComponent2::GetResultViewType2</b> and <b>IComponent2::RestoreResultView</b> methods, see 
<a href="https://msdn.microsoft.com/dee09c50-76f1-4186-846c-1cde3d05fd03">Restoring Result Views</a>.

If the snap-in is implementing an OCX (ActiveX control) view, then the snap-in creates the OCX and provides MMC with the OCX 
<a href="_com_iunknown">IUnknown</a> pointer in the <a href="https://msdn.microsoft.com/50357902-6999-4d65-8e12-81277b66d5ee">RESULT_VIEW_TYPE_INFO</a> structure (specifically, the structure's <b>pUnkControl</b> member). The snap-in has control over the OCX creation, so the snap-in can address licensing or security issues as required. During the call to 
<b>GetResultViewType2</b>, the snap-in can also initialize the OCX (the snap-in will not receive a <a href="https://msdn.microsoft.com/79256d4a-a936-419e-a953-80d743d05290">MMCN_INITOCX</a> notification).




## -see-also




<a href="https://msdn.microsoft.com/fe9a71c7-eaa6-4479-8337-0746a784a57f">IComponent2::RestoreResultView</a>



<a href="https://msdn.microsoft.com/50357902-6999-4d65-8e12-81277b66d5ee">RESULT_VIEW_TYPE_INFO</a>



<a href="https://msdn.microsoft.com/dee09c50-76f1-4186-846c-1cde3d05fd03">Restoring Result Views</a>
 

 

