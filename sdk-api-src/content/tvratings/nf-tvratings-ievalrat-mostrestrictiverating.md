---
UID: NF:tvratings.IEvalRat.MostRestrictiveRating
title: IEvalRat::MostRestrictiveRating
author: windows-sdk-content
description: The MostRestrictiveRating method compares two ratings and returns the more restrictive of the two.
old-location: mstv\ievalrat_mostrestrictiverating.htm
tech.root: MSTV
ms.assetid: b744715f-53a8-4011-9657-d2962f0e7f6e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IEvalRat interface [Microsoft TV Technologies],MostRestrictiveRating method, IEvalRat.MostRestrictiveRating, IEvalRat::MostRestrictiveRating, IEvalRatMostRestrictiveRating, MostRestrictiveRating, MostRestrictiveRating method [Microsoft TV Technologies], MostRestrictiveRating method [Microsoft TV Technologies],IEvalRat interface, mstv.ievalrat_mostrestrictiverating, tvratings/IEvalRat::MostRestrictiveRating
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tvratings.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
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
 - Tvratings.h
api_name:
 - IEvalRat.MostRestrictiveRating
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEvalRat::MostRestrictiveRating


## -description


The <b>MostRestrictiveRating</b> method compares two ratings and returns the more restrictive of the two.


## -parameters




### -param enSystem1 [in]

The rating system of the first rating to compare, specified as a member of the <a href="https://msdn.microsoft.com/646927ad-569a-4484-a3ce-6d121210b6be">EnTvRat_System</a> enumeration.


### -param enEnLevel1 [in]

The rating level of the first rating, specified as a member of the <a href="https://msdn.microsoft.com/f96a8f1a-d8e2-4976-92e3-719f0039d2a8">EnTvRat_GenericLevel</a> enumeration.
          


### -param lbfEnAttr1 [in]

Specifies the content attributes of the first rating, as a bitwise combination of flags from the <a href="https://msdn.microsoft.com/eb7f56c4-1d48-43f9-a691-c08aee3cd537">BfEnTvRat_GenericAttributes</a> enumeration.
          


### -param enSystem2 [in]

The rating system of the second rating to compare, specified as a member of the <a href="https://msdn.microsoft.com/646927ad-569a-4484-a3ce-6d121210b6be">EnTvRat_System</a> enumeration.
          


### -param enEnLevel2 [in]

The rating level of the second rating, specified as a member of the <a href="https://msdn.microsoft.com/f96a8f1a-d8e2-4976-92e3-719f0039d2a8">EnTvRat_GenericLevel</a> enumeration.
          


### -param lbfEnAttr2 [in]

Specifies the content attributes of the second rating, as a bitwise combination of flags from the <a href="https://msdn.microsoft.com/eb7f56c4-1d48-43f9-a691-c08aee3cd537">BfEnTvRat_GenericAttributes</a> enumeration.
          


### -param penSystem [out]

Receives the rating system of the more restrictive rating.
          


### -param penEnLevel [out]

Receives the rating level of the more restrictive rating.
          


### -param plbfEnAttr [out]

Receives a bitwise combination of flags from the <a href="https://msdn.microsoft.com/eb7f56c4-1d48-43f9-a691-c08aee3cd537">BfEnTvRat_GenericAttributes</a> enumeration.
          


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The ratings are from two different rating systems.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



This method enables the client to determine which of two ratings is more restrictive. For example, in the MPAA system, PG is more restrictive than R. The more restrictive rating is returned in the <i>penSystem</i>, <i>penEnLevel</i>, and <i>plbfEnAttr</i> parameters.

When the method compares ratings from two different ratings systems, it returns a rating expressed in the first system, unless the first system is unknown (TvRat_SystemDontKnow). In that case, it returns a rating using the second system.

The method returns S_FALSE if the ratings systems are not the same. There may not be an exact mapping between the two systems.




## -see-also




<a href="https://msdn.microsoft.com/b37c7e7d-80fd-4a42-a698-c20ffb2a5052">IEvalRat Interface</a>
 

 

