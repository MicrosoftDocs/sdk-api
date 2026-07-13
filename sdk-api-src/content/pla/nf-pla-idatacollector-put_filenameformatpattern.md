---
UID: NF:pla.IDataCollector.put_FileNameFormatPattern
title: IDataCollector::put_FileNameFormatPattern (pla.h)
description: Retrieves or sets the format pattern to use when decorating the file name. (Put)
helpviewer_keywords: ["FileNameFormatPattern property [PLA]","FileNameFormatPattern property [PLA]","IDataCollector interface","IDataCollector interface [PLA]","FileNameFormatPattern property","IDataCollector.FileNameFormatPattern","IDataCollector.put_FileNameFormatPattern","IDataCollector::FileNameFormatPattern","IDataCollector::get_FileNameFormatPattern","IDataCollector::put_FileNameFormatPattern","base.idatacollector_filenameformatpattern","pla.idatacollector_filenameformatpattern","pla/IDataCollector::FileNameFormatPattern","pla/IDataCollector::get_FileNameFormatPattern","pla/IDataCollector::put_FileNameFormatPattern","put_FileNameFormatPattern"]
old-location: pla\idatacollector_filenameformatpattern.htm
tech.root: PLA
ms.assetid: 94e6bb13-fb99-4968-8a7f-fbda1f6ea42e
ms.date: 12/05/2018
ms.keywords: FileNameFormatPattern property [PLA], FileNameFormatPattern property [PLA],IDataCollector interface, IDataCollector interface [PLA],FileNameFormatPattern property, IDataCollector.FileNameFormatPattern, IDataCollector.put_FileNameFormatPattern, IDataCollector::FileNameFormatPattern, IDataCollector::get_FileNameFormatPattern, IDataCollector::put_FileNameFormatPattern, base.idatacollector_filenameformatpattern, pla.idatacollector_filenameformatpattern, pla/IDataCollector::FileNameFormatPattern, pla/IDataCollector::get_FileNameFormatPattern, pla/IDataCollector::put_FileNameFormatPattern, put_FileNameFormatPattern
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Pla.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDataCollector::put_FileNameFormatPattern
 - pla/IDataCollector::put_FileNameFormatPattern
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IDataCollector.FileNameFormatPattern
 - IDataCollector.get_FileNameFormatPattern
 - IDataCollector.put_FileNameFormatPattern
---

# IDataCollector::put_FileNameFormatPattern


## -description

Retrieves or sets the format pattern to use when decorating the file name.

This property is read/write.

## -parameters

## -remarks

PLA uses the pattern only if the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_filenameformat">IDataCollector::FileNameFormat</a> property is set to <b>plaPattern</b>.

PLA appends the decoration to the file name. Use the following pattern characters to define your own pattern. For example, the pattern "MMMM d, yyyy \a\t h:mmTt" could yield "January 31, 2005 at 4:20AM". If the file name is MyFile, the decorated file name would be "MyFile January 31, 2005 at 4:20AM".

<table>
<tr>
<th>Pattern</th>
<th>Description</th>
</tr>
<tr>
<td>D</td>
<td>Day of the year.</td>
</tr>
<tr>
<td>DDD</td>
<td>Day of the year with leading zeros, if applicable.</td>
</tr>
<tr>
<td>d</td>
<td>Day of the month.</td>
</tr>
<tr>
<td>dd</td>
<td>Day of the month with a leading zero, if applicable.</td>
</tr>
<tr>
<td>ddd</td>
<td>The abbreviated name of the weekday, for example, Tue for Tuesday.</td>
</tr>
<tr>
<td>dddd</td>
<td>Full name of the weekday.</td>
</tr>
<tr>
<td>M</td>
<td>Month.</td>
</tr>
<tr>
<td>MM</td>
<td>Month with leading zero, if applicable.</td>
</tr>
<tr>
<td>MMM</td>
<td>The abbreviated name of the month, for example, Jan for January.</td>
</tr>
<tr>
<td>MMMM</td>
<td>Full name of the month.</td>
</tr>
<tr>
<td>y</td>
<td>Year without the century.</td>
</tr>
<tr>
<td>yy</td>
<td>Year without the century but including a leading zero, if applicable.</td>
</tr>
<tr>
<td>yyyy</td>
<td>Year with the century.</td>
</tr>
<tr>
<td>h</td>
<td>Hour in a 12-hour clock.</td>
</tr>
<tr>
<td>hh</td>
<td>Hour in a 12-hour clock with a leading zero, if applicable.</td>
</tr>
<tr>
<td>H</td>
<td>Hour in a 24-hour clock.</td>
</tr>
<tr>
<td>HH</td>
<td>Hour in a 24-hour clock with a leading zero, if applicable.</td>
</tr>
<tr>
<td>m</td>
<td>Minute.</td>
</tr>
<tr>
<td>mm</td>
<td>Minute with a leading zero, if applicable.</td>
</tr>
<tr>
<td>S</td>
<td>Second.</td>
</tr>
<tr>
<td>Ss</td>
<td>Second with a leading zero, if applicable.</td>
</tr>
<tr>
<td>T</td>
<td>The first character of the A.M./P.M. designator.</td>
</tr>
<tr>
<td>Tt</td>
<td>The A.M./P.M. designator.</td>
</tr>
<tr>
<td>Z</td>
<td>Time zone offset.</td>
</tr>
<tr>
<td>Zz</td>
<td>Time zone offset with a leading zero, if applicable.</td>
</tr>
<tr>
<td>N</td>
<td>Serial number. The number of leading zeros is defined by the number of characters. For example, if the serial number is 32 and the pattern is NNN, the serial number used is 032.</td>
</tr>
<tr>
<td>\c</td>
<td>Escaped character, where <i>c</i> is any character. Unrecognized characters, excluding white space, that are not escaped will result in an error.</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollector">IDataCollector</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_filename">IDataCollector::FileName</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_filenameformat">IDataCollector::FileNameFormat</a>
