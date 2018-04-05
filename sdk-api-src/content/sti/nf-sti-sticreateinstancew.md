---
UID: NF:sti.StiCreateInstanceW
title: StiCreateInstanceW function
author: windows-driver-content
description: The StiCreateInstance function is used to obtain a pointer to the IStillImage interface.
old-location: stillimg\sticreateinstance.htm
old-project: StillImg
ms.assetid: dff6e565-8faa-4fb9-ab90-5106c4d977f2
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: StiCreateInstance, StiCreateInstance function [Still Image], StiCreateInstanceA, StiCreateInstanceW, _color_StiCreateInstance, sti/StiCreateInstance, sti/StiCreateInstanceA, sti/StiCreateInstanceW, stillimg.sticreateinstance
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: sti.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StiCreateInstanceW (Unicode) and StiCreateInstanceA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SEC_WINNT_CREDUI_CONTEXT_VECTOR, *PSEC_WINNT_CREDUI_CONTEXT_VECTOR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	sti.dll
api_name:
-	StiCreateInstance
-	StiCreateInstanceA
-	StiCreateInstanceW
product: Windows
targetos: Windows
req.lib: Sti.lib
req.dll: Sti.dll
req.irql: 
req.product: Internet Explorer 6.01
---

# StiCreateInstanceW function


## -description


The <b>StiCreateInstance</b> function is used to obtain a pointer to the <b>IStillImage</b> interface. 
		All other Still Image methods are called through the pointer obtained from this function. 
		Calling this function is similar to calling the standard COM 
		<a href="_com_CoCreateInstance">CoCreateInstance</a> and 
		<a href="_com_CoInitialize">CoInitialize</a> functions.


## -parameters




### -param hinst [in]

Instance handle to the application or DLL that creates the <b>IStillImage</b> object.

STI uses this value to determine whether the application or DLL has been certified.


### -param dwVer [in]

Version number of the Sti.h header file that was used. This value must be <b>STI_VERSION</b>. Still Image uses this value to determine for what version of STI the application or DLL was designed.


### -param ppSti [out]

Pointer to a pointer to the <b>IStillImage</b> interface. This is an output parameter. When the function returns, this parameter contains a pointer to an <b>IStillImage</b> interface if the function is successful.


### -param punkOuter [in]

Pointer to the controlling <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of the COM aggregate object, or <b>NULL</b> if the interface is not aggregated. 
			 Most callers pass <b>NULL</b>. 
			 See the section on <a href="_com_aggregation">Aggregation</a> in Component Services for more information.

<div class="alert"><b>Note</b>  If aggregation is requested, the object returned in <i>ppSti</i> is a pointer to an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> rather than an <b>IStillImage</b> , as required by COM aggregation.</div>
<div> </div>

## -returns



If the function succeeds, the return value is <b>S_OK</b>.

If the function fails, the return value is the appropriate COM error.




## -remarks



Calling this function with <i>punkOuter</i> = <b>NULL</b> is similar to creating the object with <code>CoCreateInstance (&amp;CLSID_Sti, punkOuter, CLSCTX_INPROC_SERVER, &amp;IID_IStillImage, ppSti);</code> then initializing it with <a href="_com_CoInitialize">CoInitialize</a>.

Calling this function with <i>punkOuter</i> != <b>NULL</b> is similar to creating the object with <code>CoCreateInstance (&amp;CLSID_Sti, punkOuter, CLSCTX_INPROC_SERVER, &amp;IID_IUnknown, ppSti)</code>. The aggregated object must be initialized manually.




## -see-also




<a href="https://msdn.microsoft.com/d601500a-80d7-4b86-aeaa-1a32dd7420a4">About Still Image</a>



<a href="https://msdn.microsoft.com/6fa6af12-4aea-4143-af8e-967473b571b4">Making an Application Still Image-Aware</a>
 

 

