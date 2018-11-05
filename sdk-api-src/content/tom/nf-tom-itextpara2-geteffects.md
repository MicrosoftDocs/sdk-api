---
UID: NF:tom.ITextPara2.GetEffects
title: ITextPara2::GetEffects
author: windows-sdk-content
description: Gets the paragraph format effects.
old-location: controls\itextpara2_geteffects.htm
tech.root: controls
ms.assetid: 7f672cc9-e8f3-416a-8f41-9b71ca1858a1
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetEffects, GetEffects method [Windows Controls], GetEffects method [Windows Controls],ITextPara2 interface, ITextPara2 interface [Windows Controls],GetEffects method, ITextPara2.GetEffects, ITextPara2::GetEffects, controls.itextpara2_geteffects, tom/ITextPara2::GetEffects, tomParaEffectBox, tomParaEffectCollapsed, tomParaEffectDoNotHyphen, tomParaEffectKeep, tomParaEffectKeepNext, tomParaEffectNoLineNumber, tomParaEffectNoWidowControl, tomParaEffectOutlineLevel, tomParaEffectPageBreakBefore, tomParaEffectRTL, tomParaEffectSideBySide, tomParaEffectTable, tomParaEffectTableRowDelimiter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: Msftedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextPara2.GetEffects
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextPara2::GetEffects


## -description


Gets the paragraph format effects.


## -parameters




### -param pValue [out]

Type: <b>long*</b>

The paragraph effects. This value can be a combination of the following flags. 


<a id="tomParaEffectRTL"></a>
<a id="tomparaeffectrtl"></a>
<a id="TOMPARAEFFECTRTL"></a>


#### tomParaEffectRTL

<a id="tomParaEffectKeep"></a>
<a id="tomparaeffectkeep"></a>
<a id="TOMPARAEFFECTKEEP"></a>


#### tomParaEffectKeep

<a id="tomParaEffectKeepNext"></a>
<a id="tomparaeffectkeepnext"></a>
<a id="TOMPARAEFFECTKEEPNEXT"></a>


#### tomParaEffectKeepNext

<a id="tomParaEffectPageBreakBefore"></a>
<a id="tomparaeffectpagebreakbefore"></a>
<a id="TOMPARAEFFECTPAGEBREAKBEFORE"></a>


#### tomParaEffectPageBreakBefore

<a id="tomParaEffectNoLineNumber"></a>
<a id="tomparaeffectnolinenumber"></a>
<a id="TOMPARAEFFECTNOLINENUMBER"></a>


#### tomParaEffectNoLineNumber

<a id="tomParaEffectNoWidowControl"></a>
<a id="tomparaeffectnowidowcontrol"></a>
<a id="TOMPARAEFFECTNOWIDOWCONTROL"></a>


#### tomParaEffectNoWidowControl

<a id="tomParaEffectDoNotHyphen"></a>
<a id="tomparaeffectdonothyphen"></a>
<a id="TOMPARAEFFECTDONOTHYPHEN"></a>


#### tomParaEffectDoNotHyphen

<a id="tomParaEffectSideBySide"></a>
<a id="tomparaeffectsidebyside"></a>
<a id="TOMPARAEFFECTSIDEBYSIDE"></a>


#### tomParaEffectSideBySide

<a id="tomParaEffectCollapsed"></a>
<a id="tomparaeffectcollapsed"></a>
<a id="TOMPARAEFFECTCOLLAPSED"></a>


#### tomParaEffectCollapsed

<a id="tomParaEffectOutlineLevel"></a>
<a id="tomparaeffectoutlinelevel"></a>
<a id="TOMPARAEFFECTOUTLINELEVEL"></a>


#### tomParaEffectOutlineLevel

<a id="tomParaEffectBox"></a>
<a id="tomparaeffectbox"></a>
<a id="TOMPARAEFFECTBOX"></a>


#### tomParaEffectBox

<a id="tomParaEffectTableRowDelimiter"></a>
<a id="tomparaeffecttablerowdelimiter"></a>
<a id="TOMPARAEFFECTTABLEROWDELIMITER"></a>


#### tomParaEffectTableRowDelimiter

<a id="tomParaEffectTable"></a>
<a id="tomparaeffecttable"></a>
<a id="TOMPARAEFFECTTABLE"></a>


#### tomParaEffectTable


### -param pMask [out]

Type: <b>long*</b>

The differences in the flags over the range. A value of 1 indicates that the corresponding effect is the same over the range. For an insertion point, the values equal 1 for all defined effects. 



## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



If the <b>tomTable</b> flag is set, you can use the  <a href="https://msdn.microsoft.com/ade77edf-6a9e-4c8d-a522-3158c802b6dd">ITextRange2::GetTable</a> method to get more table properties.




## -see-also




<a href="https://msdn.microsoft.com/31a0849f-c651-4178-b1ff-a4333bcde5d9">ITextPara2</a>



<a href="https://msdn.microsoft.com/e7184de4-b416-4f28-8f10-c89ffcccf1a1">ITextPara2::SetEffects</a>
 

 

